<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hollard Brand Campaign Dashboard</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/chartjs-plugin-datalabels@2.0.0"></script>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #1a0f2e;
            color: #ffffff;
            margin: 0;
            padding: 20px;
        }
        .dashboard-header {
            background-color: #2c1e4a;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        .dashboard-title {
            text-align: center;
            font-size: 28px;
            font-weight: 600;
            margin-bottom: 20px;
            color: #fff;
        }
        .month-tabs, .view-tabs {
            display: flex;
            justify-content: center;
            margin-bottom: 20px;
        }
        .month-tab, .view-tab {
            background-color: #3c2b5a;
            color: #fff;
            border: none;
            padding: 10px 20px;
            margin: 0 5px;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        .month-tab.active, .view-tab.active {
            background-color: #8e44ad;
        }
        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(450px, 1fr));
            gap: 20px;
        }
        .chart-container {
            background-color: #3c2b5a;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        .chart-title {
            text-align: center;
            margin-bottom: 15px;
            font-size: 20px;
            font-weight: 600;
            color: #fff;
        }
        .kpi-container {
            display: flex;
            justify-content: space-around;
            margin-bottom: 20px;
        }
        .kpi-item {
            text-align: center;
            background-color: #3c2b5a;
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        .kpi-title {
            font-size: 16px;
            font-weight: 600;
            margin-bottom: 5px;
        }
        .kpi-value {
            font-size: 24px;
            font-weight: 600;
        }
        .kpi-change {
            font-size: 14px;
            margin-top: 5px;
        }
        .positive-change {
            color: #4caf50;
        }
        .negative-change {
            color: #f44336;
        }
        .excel-view {
            background-color: #3c2b5a;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            overflow-x: auto;
        }
        .excel-table {
            width: 100%;
            border-collapse: collapse;
        }
        .excel-table th, .excel-table td {
            border: 1px solid #ffffff;
            padding: 8px;
            text-align: left;
        }
        .excel-table th {
            background-color: #8e44ad;
        }
        .excel-chart {
            margin-top: 20px;
            height: 300px;
        }
    </style>
</head>
<body>
    <div class="dashboard-header">
        <div class="dashboard-title">Hollard Brand Campaign Dashboard</div>
        <div class="view-tabs">
            <button class="view-tab active" data-view="charts">Charts View</button>
            <button class="view-tab" data-view="excel">Excel View</button>
        </div>
    </div>
    <div class="kpi-container">
        <div class="kpi-item">
            <div class="kpi-title">Total Engagement</div>
            <div class="kpi-value" id="total-engagement">1,394</div>
            <div class="kpi-change positive-change" id="engagement-change">+5.2%</div>
        </div>
        <div class="kpi-item">
            <div class="kpi-title">Total Views</div>
            <div class="kpi-value" id="total-views">1,245,000</div>
            <div class="kpi-change positive-change" id="views-change">+12.8%</div>
        </div>
        <div class="kpi-item">
            <div class="kpi-title">Avg. Engagement Rate</div>
            <div class="kpi-value" id="avg-engagement-rate">3.7%</div>
            <div class="kpi-change negative-change" id="engagement-rate-change">-0.3%</div>
        </div>
    </div>
    <div id="charts-view" class="grid-container">
        <div class="chart-container">
            <div class="chart-title">Total Engagement by Platform</div>
            <canvas id="engagementChart"></canvas>
        </div>
        <div class="chart-container">
            <div class="chart-title">Views Comparison</div>
            <canvas id="viewsChart"></canvas>
        </div>
        <div class="chart-container">
            <div class="chart-title">Likes Growth</div>
            <canvas id="likesChart"></canvas>
        </div>
        <div class="chart-container">
            <div class="chart-title">Shares Distribution</div>
            <canvas id="sharesChart"></canvas>
        </div>
    </div>
    <div id="excel-view" class="excel-view" style="display: none;">
        <table class="excel-table" id="excel-table">
            <!-- Table content will be dynamically generated -->
        </table>
        <div class="excel-chart">
            <canvas id="excelChart"></canvas>
        </div>
    </div>

    <script>
        Chart.register(ChartDataLabels);

        // Complete data from January to October
        const data = {
            'January': {
                platforms: ['Facebook', 'Instagram', 'LinkedIn', 'YouTube'],
                likes: [0, 0, 0, 0],
                comments: [0, 0, 0, 0],
                shares: [0, 0, 0, 0],
                views: [0, 0, 0, 0]
            },
            'February': {
                platforms: ['Facebook', 'Instagram', 'LinkedIn', 'YouTube'],
                likes: [0, 0, 0, 0],
                comments: [0, 0, 0, 0],
                shares: [0, 0, 0, 0],
                views: [0, 0, 0, 0]
            },
            'March': {
                platforms: ['Facebook', 'Instagram', 'LinkedIn', 'YouTube'],
                likes: [0, 0, 0, 0],
                comments: [0, 0, 0, 0],
                shares: [0, 0, 0, 0],
                views: [0, 0, 0, 0]
            },
            'April': {
                platforms: ['Facebook', 'Instagram', 'LinkedIn', 'YouTube'],
                likes: [0, 0, 0, 0],
                comments: [0, 0, 0, 0],
                shares: [0, 0, 0, 0],
                views: [0, 0, 0, 0]
            },
            'May': {
                platforms: ['Facebook', 'Instagram', 'LinkedIn', 'YouTube'],
                likes: [0, 0, 0, 0],
                comments: [0, 0, 0, 0],
                shares: [0, 0, 0, 0],
                views: [0, 0, 0, 0]
            },
            'June': {
                platforms: ['Facebook', 'Instagram', 'LinkedIn', 'YouTube'],
                likes: [0, 0, 0, 0],
                comments: [0, 0, 0, 0],
                shares: [0, 0, 0, 0],
                views: [0, 0, 0, 0]
            },
            'July': {
                platforms: ['Facebook', 'Instagram', 'LinkedIn', 'YouTube'],
                likes: [0, 0, 0, 0],
                comments: [0, 0, 0, 0],
                shares: [0, 0, 0, 0],
                views: [0, 0, 0, 0]
            },
            'August': {
                platforms: ['Facebook', 'Instagram', 'LinkedIn', 'YouTube'],
                likes: [0, 0, 0, 0],
                comments: [0, 0, 0, 0],
                shares: [0, 0, 0, 0],
                views: [0, 0, 0, 0]
            },
            'September': {
                platforms: ['Facebook', 'Instagram', 'LinkedIn', 'YouTube'],
                likes: [123, 121, 408, 29],
                comments: [16, 0, 32, 6],
                shares: [73, 33, 81, 0],
                views: [5900, 2700, 12500, 1100]
            },
            'October': {
                platforms: ['Facebook', 'Instagram', 'LinkedIn', 'YouTube'],
                likes: [124, 126, 426, 37],
                comments: [17, 3, 32, 8],
                shares: [73, 33, 83, 0],
                views: [7600, 2700, 12500, 1200000]
            }
        };

        const months = ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October'];

        const chartColors = {
            'Facebook': '#4267B2',
            'Instagram': '#E1306C',
            'LinkedIn': '#0077B5',
            'YouTube': '#FF0000'
        };

        const commonOptions = {
            responsive: true,
            plugins: {
                legend: {
                    position: 'top',
                    labels: {
                        color: '#ffffff',
                        font: {
                            size: 12
                        }
                    }
                },
                datalabels: {
                    color: '#ffffff',
                    anchor: 'end',
                    align: 'top',
                    formatter: (value) => value.toLocaleString()
                }
            },
            scales: {
                x: {
                    ticks: { color: '#ffffff' }
                },
                y: {
                    ticks: { color: '#ffffff' }
                }
            }
        };

        function createChart(ctx, type, labels, datasets) {
            return new Chart(ctx, {
                type: type,
                data: {
                    labels: labels,
                    datasets: datasets
                },
                options: commonOptions
            });
        }

        // Generate Excel Table
        function generateExcelTable() {
            const table = document.getElementById('excel-table');
            const headerRow = `<tr>
                <th>Month</th>
                <th>Platform</th>
                <th>Likes</th>
                <th>Comments</th>
                <th>Shares</th>
                <th>Views</th>
            </tr>`;
            table.innerHTML = headerRow;

            months.forEach(month => {
                data[month].platforms.forEach((platform, index) => {
                    const row = `<tr>
                        <td>${month}</td>
                        <td>${platform}</td>
                        <td>${data[month].likes[index]}</td>
                        <td>${data[month].comments[index]}</td>
                        <td>${data[month].shares[index]}</td>
                        <td>${data[month].views[index]}</td>
                    </tr>`;
                    table.innerHTML += row;
                });
            });
        }

        document.addEventListener('DOMContentLoaded', () => {
            // Engagement Chart
            createChart(
                document.getElementById('engagementChart'),
                'bar',
                months,
                data['September'].platforms.map((platform, i) => ({
                    label: platform,
                    data: months.map(month => data[month].likes[i] + data[month].comments[i] + data[month].shares[i]),
                    backgroundColor: chartColors[platform],
                }))
            );

            // Views Chart
            createChart(
                document.getElementById('viewsChart'),
                'bar',
                months,
                data['September'].platforms.map((platform, i) => ({
                    label: platform,
                    data: months.map(month => data[month].views[i]),
                    backgroundColor: chartColors[platform],
                }))
            );

            // Likes Chart
            createChart(
                document.getElementById('likesChart'),
                'line',
                months,
                data['September'].platforms.map((platform, i) => ({
                    label: platform,
                    data: months.map(month => data[month].likes[i]),
                    borderColor: chartColors[platform],
                    backgroundColor: chartColors[platform],
                    tension: 0.1,
                    fill: false
                }))
            );

            // Shares Chart
            createChart(
                document.getElementById('sharesChart'),
                'pie',
                months,
                data['September'].platforms.map((platform, i) => ({
                    label: platform,
                    data: months.map(month => data[month].shares[i]),
                    backgroundColor: chartColors[platform],
                }))
            );

            // Excel Table and Chart generation
            generateExcelTable();

            // View toggle
            document.querySelectorAll('.view-tab').forEach(tab => {
                tab.addEventListener('click', (e) => {
                    document.querySelectorAll('.view-tab').forEach(t => t.classList.remove('active'));
                    e.target.classList.add('active');
                    const view = e.target.dataset.view;
                    document.getElementById('charts-view').style.display = view === 'charts' ? 'grid' : 'none';
                    document.getElementById('excel-view').style.display = view === 'excel' ? 'block' : 'none';
                });
            });
        });
    </script>
</body>
</html>
