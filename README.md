# PropertyFinder
This contains few automation examples on Property Finder website using Selenium, Cucumber and Serenity

# Prerequisites : -
•	Should have java installed
•	Should have maven installed

# Execute Test : -
The Default Browser used is Chrome

•	mvn clean test

If User Wants to specify the browser than he must use

•	For Chrome

    mvn clean verify -P chrome

•	For Firefox

    mvn clean verify -P firefox

•	For Headless

    mvn clean verify -P phantom.js

# Please Note : -

Since the drivers used for windows and mac are different If the user wishes to run the test pack on mac than he has to make the following changes

•	Traverse to pom.xml and remove .exe from all the following : -

     • src/test/resources/driver/geckodriver.exe

     • src/test/resources/driver/chromedriver.exe

     • src/test/resources/driver/phantomjs.exe

# Execution Results : -

An html file is generated at "target/site/index.html"

<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8"/>

    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <title>Serenity Reports</title>

    <link rel="shortcut icon" type="image/x-icon" href="/favicon.ico">
<link rel="apple-touch-icon" sizes="57x57" href="/apple-icon-57x57.png">
<link rel="apple-touch-icon" sizes="60x60" href="/apple-icon-60x60.png">
<link rel="apple-touch-icon" sizes="72x72" href="/apple-icon-72x72.png">
<link rel="apple-touch-icon" sizes="76x76" href="/apple-icon-76x76.png">
<link rel="apple-touch-icon" sizes="114x114" href="/apple-icon-114x114.png">
<link rel="apple-touch-icon" sizes="120x120" href="/apple-icon-120x120.png">
<link rel="apple-touch-icon" sizes="144x144" href="/apple-icon-144x144.png">
<link rel="apple-touch-icon" sizes="152x152" href="/apple-icon-152x152.png">
<link rel="apple-touch-icon" sizes="180x180" href="/apple-icon-180x180.png">
<link rel="icon" type="image/png" sizes="192x192"  href="/android-icon-192x192.png">
<link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="96x96" href="/favicon-96x96.png">
<link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
<meta name="msapplication-TileColor" content="#ffffff">
<meta name="msapplication-TileImage" content="/ms-icon-144x144.png">
<meta name="theme-color" content="#ffffff">
<link rel="stylesheet" href="font-awesome/css/font-awesome.min.css">
<!--[if IE 7]>
<link rel="stylesheet" href="font-awesome/css/font-awesome-ie7.min.css">
<![endif]--><!-- JQuery -->
<script type="text/javascript" src="scripts/jquery-1.11.1.min.js"></script><!-- Bootstrap -->
<link href="bootstrap/css/bootstrap.min.css" rel="stylesheet">
<script src="bootstrap/js/bootstrap.min.js"></script><link rel="stylesheet" href="css/core.css"/>
<link rel="stylesheet" href="css/link.css"/>
<link type="text/css" media="screen" href="css/screen.css" rel="Stylesheet"/><!-- JQuery-UI -->
<link type="text/css" href="jqueryui/1.11.2-start/jquery-ui.min.css" rel="Stylesheet" />
<script type="text/javascript" src="jqueryui/1.11.2-start/jquery-ui.min.js"></script><!-- DataTables -->
<link type="text/css" href="datatables/1.10.4/media/jqueryui/dataTables.jqueryui.css" rel="Stylesheet"/>
<link type="text/css" href="css/tables.css" rel="stylesheet" />

<script type="text/javascript" src="datatables/1.10.4/media/js/jquery.dataTables.min.js"></script>
<script type="text/javascript" src="datatables/1.10.4/media/jqueryui/dataTables.jqueryui.min.js"></script><!-- jQplot -->
<!--[if IE]>
<script language="javascript" type="text/javascript" src="excanvas/3/excanvas.compiled.js"></script>
<![endif]--><link rel="stylesheet" type="text/css" href="jqplot/1.0.8/jquery.jqplot.min.css"/>
<script type="text/javascript" src="jqplot/1.0.8/jquery.jqplot.min.js"></script>
<script type="text/javascript" src="jqplot/1.0.8/plugins/jqplot.pieRenderer.min.js"></script>




    <script class="code" type="text/javascript">$(document).ready(function () {
        var test_results_plot = $.jqplot('test_results_pie_chart', [
            [
                ['Passing', 0.75],

                ['Pending', 0],

                ['Ignored/Skipped', 0],

                ['Failing', 0],

                ['Errors',  0.25],
                ['Compromised',  0]
            ]
        ], {

            gridPadding: {top: 0, bottom: 38, left: 0, right: 0},
            seriesColors: ['#30cb23',

                '#a2f2f2',

                '#eeeadd',

                '#f8001f',

                '#fc6e1f',
                'fuchsia'],
            seriesDefaults: {
                renderer: $.jqplot.PieRenderer,
                trendline: { show: false },
                rendererOptions: { padding: 8, showDataLabels: true }
            },
            legend: {
                show: true,
                placement: 'outside',
                rendererOptions: {
                    numberRows: 2
                },
                location: 's',
                marginTop: '15px'
            },
            series: [
                {label: '3 / 4 tests passed' },
                {label: '0 / 4 tests pending'},
                {label: '0 / 4 tests not executed'},
                {label: '0 / 4 tests failed'},
                {label: '1 / 4 errors'},
                {label: '0 / 4 compromised tests'}
            ]
        });

        var weighted_test_results_plot = $.jqplot('weighted_test_results_pie_chart', [
            [
                ['Passing', 0.777778],

                ['Pending', 0],

                ['Ignored', 0],

                ['Failing', 0],

                ['Errors', 0.222222],
                ['Compromised', 0],
            ]
        ], {

            gridPadding: {top: 0, bottom: 38, left: 0, right: 0},
            seriesColors: ['#30cb23',

                '#a2f2f2',

                '#eeeadd',

                '#f8001f',

                '#fc6e1f',
                'mediumvioletred'],

            seriesDefaults: {
                renderer: $.jqplot.PieRenderer,
                trendline: { show: false },
                rendererOptions: { padding: 8, showDataLabels: true }
            },
            legend: {
                show: true,
                placement: 'outside',
                rendererOptions: {
                    numberRows: 2
                },
                location: 's',
                marginTop: '15px'
            },
            series: [
                {label: '3 / 4 tests passed (0.777778% of all test steps)' },
                {label: '0 / 4 tests pending'},
                {label: '0 / 4 tests not executed'},
                {label: '0 / 4 tests failed (0% of all test steps)'},
                {label: '1 / 4 errors (0.222222% of all test steps)'}
            ]
        });

        // Results table
        $('#test-results-table').DataTable({
            "order": [
                [ 1, "asc" ]
            ],
            "pageLength": 100,
            "lengthMenu": [ [50, 100, 200, -1] , [50, 100, 200, "All"] ]
        });

        // Pie charts
        $('#test-results-tabs').tabs();

        $('#toggleNormalPieChart').click(function () {
            $("#test_results_pie_chart").toggle();
        });

        $('#toggleWeightedPieChart').click(function () {
            $("#weighted_test_results_pie_chart").toggle();
        });



    })
    ;
    </script>
</head>

<body class="results-page">
<div id="topheader">
    <div id="topbanner">
        <div id="logo"><a href="index.html"><img src="images/serenity-logo.png" border="0"/></a></div>
        <div id="projectname-banner" style="float:right">
            <span class="projectname">Interview Test For PropertyFinder</span>
        </div>
    </div>
</div>

<div class="middlecontent">

<div id="contenttop">
    <div class="middlebg">
        <span class="breadcrumbs"><a href="index.html">Home</a>
        </span>
    </div>
    <div class="rightbg"></div>
</div>

<div class="clr"></div>

<!--/* starts second table*/-->
<div>
    <ul class="nav nav-tabs" role="tablist">
        <li class="active">
            <a href="#"><i class="fa fa-check-square-o"></i> Overall Test Results</a>
        </li>
        <li >
            <a href="capabilities.html"><i class="fa fa-book"></i> Requirements</a>
        </li>
        <li >
            <a href="576946480b52ad056d6f5bddf874399c83582ecf90963cc074a14c70580e7d9f.html"><i class="fa fa-comments-o"></i> Features</a>
        </li>
    </ul>
    <span class="date-and-time"><a href="build-info.html"><i class="fa fa-info-circle"></i></a> Report generated 08-12-2017 19:38</span>
    <br style="clear:left"/>
</div>
<div class="clr"></div>
<div id="beforetable"></div>
<div id="results-dashboard">
<div class="middlb">
<div class="table">

<h2>Test Results: All Tests</h2>
<table class='overview'>
    <tr>
        <td width="375px" valign="top">
            <div class="test-count-summary">
                <span class="test-count-title">4
                    test scenarios (4 tests in all, including 3
                    rows of test data)</span>
                <div>

                    <span class="test-count"> |
                        3
                            <a href="01f5288b80adbd3af52a8ed68a4a616d3164f750229f80da1ef344382d948835.html">passed</a>

                    </span>
                    <span class="test-count"> |
                        1
                            <a href="b964a040ccee2192880812cc5de2c4d0075e3288c1b298b7dda0839367bb26be.html">unsuccessful</a>

                    </span>(
                    <span class="test-count">
                        0
                            <a href="da5b0c51b332adf0ef993a9f086d6a1b51a3d800248ec6ae281212092f35bd37.html">failed</a>
                        ,
                    </span>
                    <span class="test-count">
                        1
                            <a href="c8a926210aeff57f8aa7ea799262d4b730915a909cd5ecd6a705b1fa13bc7aa8.html">with errors</a>

                    </span>)





                 |
                    <a href="results.csv" title="Download CSV"> <i class="fa fa-download" title="Download CSV"></i></a>
                </div>
            </div>

            <div id="test-results-tabs">
                <ul>
                    <li><a href="#test-results-tabs-1">Test Count</a></li>
                    <li><a href="#test-results-tabs-2">Weighted Tests</a></li>
                </ul>
                <div id="test-results-tabs-1">
                    <table>
                        <tr>
                            <td colspan="2">
                                <span class="caption">Distribution of tests (including rows in data-driven tests) by test result.</span>
                                <span class="togglePieChart" id="toggleNormalPieChart"><a href="#">Show/Hide Pie Chart</a></span>
                            </td>
                        </tr>
                        <tr>
                            <td style="vertical-align: text-top;">
                                <div id="test_results_pie_chart"></div>
                            </td>
                            <td class="related-tags-section">
                                <div>





<div>
    <h4>Test Result Summary</h4>
    <table class="summary-table">
        <head>
            <tr>
                <th>Test Type</th>
                <th>Total</th>
                <th>Pass&nbsp;<i class="icon-check"/> </th>
                <th>Fail&nbsp;<i class="icon-thumbs-down"/></th>
                <th>Pending&nbsp;<i class="icon-calendar"/></th>
                <th>Ignore/Skip&nbsp;<i class="icon-ban-circle"/></th>
            </tr>
        </head>
        <body>
        <tr>
            <td class="summary-leading-column">Automated</td>
            <td>4</td>
            <td>3 (75%)</td>
            <td>1 (25%)</td>
            <td>0 (0%)</td>
            <td>0 (0%)</td>
        </tr>
        <tr>
            <td class="summary-leading-column">Manual</td>
            <td>0</td>
            <td>0 (0%)</td>
            <td>0 (0%)</td>
            <td>0 (0%)</td>
            <td>0 (0%)</td>
        </tr>
        <tr>
            <td class="summary-leading-column">Total</td>
            <td>4</td>
            <td>3 (75%)</td>
            <td>1 (25%)</td>
            <td>0 (0%)</td>
            <td>0 (0%)</td>
        </tr>
        <tr>
            <td class="summary-leading-column">Total Duration</td>
                <td colspan="5">5 minutes 49 seconds</td>
        </tr>
        </body>
    </table>
</div>                                </div>
                                <div>
<table class="tags-summary-table">
    <tr>
        <td width="300px"><h3>Related Tags</h3></td>
        <td width="90px" class="tag-count-header">% Passed</td>
        <td width="130px" class="test-count">&nbsp;</td>
        <td class="tag-count-header">Test count</td>
    </tr>
</table>
        <table class="test-summary-table">
            <tr>
                <td colspan="3">
                    <div class="tagTypeTitle">Features</div>
                </td>
            </tr>
                <tr>
                    <td class="bluetext tag-title">
                        <span class="ERROR-text truncated-tag-title">
                                <a href="4dad9bfcc1946ab5de4975aa3346dfdfe02679d6dbc71aa698e2efe502500ed5.html" title="Assesment Test For Property Finder">Assesment Test For Property Finder</a>
                        </span>
                    </td>
                    <td width="220px" class="table-figure">


                        <table>
                            <tr>
                                <td class="related-tag-percentage"><span title="3 out of 4 tests (14 steps) passing">75%</span></td>
                                <td width="150px">
                                    <a href="4dad9bfcc1946ab5de4975aa3346dfdfe02679d6dbc71aa698e2efe502500ed5.html">
                                        <div class="pendingbar"
                                             title="0 out of 4 tests (0 steps) pending"
                                             style="width: 150px;">
                                            <div class="ignoredbar"
                                                 style="width: 150px;"
                                                 title="0 out of 4 tests (0 steps) skipped or ignored">
                                                <div class="compromisedbar"
                                                     style="width: 150px;"
                                                     title="0 out of 4 tests (0 steps) compromised">
                                                    <div class="errorbar"
                                                         style="width: 150px;"
                                                         title="1 out of 4 tests (4 steps) broken">
                                                        <div class="failingbar"
                                                             style="width: 112px;"
                                                             title="0 out of 4 tests (0 steps) failing">
                                                            <div class="passingbar"
                                                                 style="width: 112px;"
                                                                 title="3 out of 4 tests (14 steps) passing">
                                                            </div>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </a>
                                </td>
                                <td class="related-tag-count"><span class="result-test-count" title="4 tests">4</span></td>
                            </tr>
                        </table>
                    </td>
                </tr>
        </table>
                                </div>
                            </td>
                        </tr>
                    </table>
                </div>
                <div id="test-results-tabs-2">
                    <table>
                        <tr>
                            <td colspan="2">
                                <span class="caption">Test results weighted by test size in steps (average steps per test: 5) .</span>
                                <span class="togglePieChart" id="toggleWeightedPieChart"><a href="#">Show/Hide Pie
                                    Chart</a></span>
                            </td>
                        </tr>
                        <tr>
                            <td style="vertical-align: text-top;">
                                <div id="weighted_test_results_pie_chart"></div>
                            </td>
                            <td class="related-tags-section">
                                <div>





<div>
    <h4>Test Result Summary</h4>
    <table class="summary-table">
        <head>
            <tr>
                <th>Test Type</th>
                <th>Total</th>
                <th>Pass&nbsp;<i class="icon-check"/> </th>
                <th>Fail&nbsp;<i class="icon-thumbs-down"/></th>
                <th>Pending&nbsp;<i class="icon-calendar"/></th>
                <th>Ignore/Skip&nbsp;<i class="icon-ban-circle"/></th>
            </tr>
        </head>
        <body>
        <tr>
            <td class="summary-leading-column">Automated</td>
            <td>4</td>
            <td>3 (75%)</td>
            <td>1 (25%)</td>
            <td>0 (0%)</td>
            <td>0 (0%)</td>
        </tr>
        <tr>
            <td class="summary-leading-column">Manual</td>
            <td>0</td>
            <td>0 (0%)</td>
            <td>0 (0%)</td>
            <td>0 (0%)</td>
            <td>0 (0%)</td>
        </tr>
        <tr>
            <td class="summary-leading-column">Total</td>
            <td>4</td>
            <td>3 (75%)</td>
            <td>1 (25%)</td>
            <td>0 (0%)</td>
            <td>0 (0%)</td>
        </tr>
        <tr>
            <td class="summary-leading-column">Total Duration</td>
                <td colspan="5">5 minutes 49 seconds</td>
        </tr>
        </body>
    </table>
</div>                                </div>
                                <div>
<table class="tags-summary-table">
    <tr>
        <td width="300px"><h3>Related Tags</h3></td>
        <td width="90px" class="tag-count-header">% Passed</td>
        <td width="130px" class="test-count">&nbsp;</td>
        <td class="tag-count-header">Test count</td>
    </tr>
</table>
        <table class="test-summary-table">
            <tr>
                <td colspan="3">
                    <div class="tagTypeTitle">Features</div>
                </td>
            </tr>
                <tr>
                    <td class="bluetext tag-title">
                        <span class="ERROR-text truncated-tag-title">
                                <a href="4dad9bfcc1946ab5de4975aa3346dfdfe02679d6dbc71aa698e2efe502500ed5.html" title="Assesment Test For Property Finder">Assesment Test For Property Finder</a>
                        </span>
                    </td>
                    <td width="220px" class="table-figure">


                        <table>
                            <tr>
                                <td class="related-tag-percentage"><span title="3 out of 4 tests (14 steps) passing">77.8%</span></td>
                                <td width="150px">
                                    <a href="4dad9bfcc1946ab5de4975aa3346dfdfe02679d6dbc71aa698e2efe502500ed5.html">
                                        <div class="pendingbar"
                                             title="0 out of 4 tests (0 steps) pending"
                                             style="width: 150px;">
                                            <div class="ignoredbar"
                                                 style="width: 150px;"
                                                 title="0 out of 4 tests (0 steps) skipped or ignored">
                                                <div class="compromisedbar"
                                                     style="width: 150px;"
                                                     title="0 out of 4 tests (0 steps) compromised">
                                                    <div class="errorbar"
                                                         style="width: 150px;"
                                                         title="1 out of 4 tests (4 steps) broken">
                                                        <div class="failingbar"
                                                             style="width: 117px;"
                                                             title="0 out of 4 tests (0 steps) failing">
                                                            <div class="passingbar"
                                                                 style="width: 117px;"
                                                                 title="3 out of 4 tests (14 steps) passing">
                                                            </div>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </a>
                                </td>
                                <td class="related-tag-count"><span class="result-test-count" title="4 tests">4</span></td>
                            </tr>
                        </table>
                    </td>
                </tr>
        </table>
                                </div>
                            </td>
                        </tr>
                    </table>
                </div>
            </div>
        </td>

    </tr>
</table>

<table>
    <tr>
        <td>
            <div><h3>Tests</h3></div>
            <div id="test_list_tests" class="table">
                <div class="test-results">
                    <table id="test-results-table">
                        <thead>
                        <tr>
                            <th width="50" class="test-results-heading">&nbsp;</th>
                            <th width="%" class="test-results-heading">Tests</th>
                            <th width="70" class="test-results-heading">Steps</th>

                            <th width="100" class="test-results-heading">Started</th>
                            <th width="100" class="test-results-heading">Took<br>(secs)</th>
                        </tr>
                        </thead>
                        <tbody>

                            <tr class="test-SUCCESS">
                                <td><span class="summary-icon"><i class='fa fa-check-square-o success-icon ' title='SUCCESS'></i></span>

                                    <span style="display:none">SUCCESS</span></td>
                                <td class="SUCCESS-text">
                                    <div class="ellipsis">

                                        <a href="c5795d95a929a7f176fd6a83e1998af87040ebe625359bca8805454206f05fb0.html" class="ellipsis"
                                           title="Fetching the agents results as per given criteria and storing the details in CSV file ">
                                            Fetching the agents results as per given criteria and storing the details in CSV file&nbsp;(1  examples)
                                                <span class="related-issue-title"></span>
                                        </a>
                                    </div>
                                </td>

                                <td class="SUCCESS-text">6</td>


                                <td class="SUCCESS-text" data-sort="2017-12-08 19:32:11">19:32:11</td>

                                <td class="SUCCESS-text">28.21</td>
                            </tr>

                            <tr class="test-SUCCESS">
                                <td><span class="summary-icon"><i class='fa fa-check-square-o success-icon ' title='SUCCESS'></i></span>

                                    <span style="display:none">SUCCESS</span></td>
                                <td class="SUCCESS-text">
                                    <div class="ellipsis">

                                        <a href="9cf3eba4dd8a81f2b4611d617ec9b6f57f463e76ad0ae2c5c956355ff033bb13.html" class="ellipsis"
                                           title="Agents Check ">
                                            Agents Check&nbsp;(1  examples)
                                                <span class="related-issue-title"></span>
                                        </a>
                                    </div>
                                </td>

                                <td class="SUCCESS-text">4</td>


                                <td class="SUCCESS-text" data-sort="2017-12-08 19:32:40">19:32:40</td>

                                <td class="SUCCESS-text">95.99</td>
                            </tr>

                            <tr class="test-SUCCESS">
                                <td><span class="summary-icon"><i class='fa fa-check-square-o success-icon ' title='SUCCESS'></i></span>

                                    <span style="display:none">SUCCESS</span></td>
                                <td class="SUCCESS-text">
                                    <div class="ellipsis">

                                        <a href="d4cce5d3b195f3873bd292eb7b72365794ebde8e17e282c4af6e280a9483246b.html" class="ellipsis"
                                           title="Capture Agent Data and store in text file ">
                                            Capture Agent Data and store in text file
                                                <span class="related-issue-title"></span>
                                        </a>
                                    </div>
                                </td>

                                <td class="SUCCESS-text">4</td>


                                <td class="SUCCESS-text" data-sort="2017-12-08 19:34:16">19:34:16</td>

                                <td class="SUCCESS-text">215</td>
                            </tr>

                            <tr class="test-ERROR">
                                <td><span class="summary-icon"><i class='fa fa-exclamation-triangle error-icon ' title='ERROR'></i></span>

                                    <span style="display:none">ERROR</span></td>
                                <td class="ERROR-text">
                                    <div class="ellipsis">

                                        <a href="8fdcbc74c0a96871372f696bd48e56d685f8a90d0655512c02910d18eab110a5.html" class="ellipsis"
                                           title="This is an example of failure to show screenshot on failed steps No such element exception: No value p...">
                                            This is an example of failure to show screenshot on failed steps&nbsp;(1  examples)
                                                <span class="related-issue-title"></span>
                                        </a>
                                    </div>
                                </td>

                                <td class="ERROR-text">4</td>


                                <td class="ERROR-text" data-sort="2017-12-08 19:37:51">19:37:51</td>

                                <td class="ERROR-text">10.67</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
        </td>
    </tr>
</table>
</div>

</div>
</div>
</div>
</div>
<div id="beforefooter"></div>
<div id="bottomfooter">
    <span class="version">Serenity version 1.8.1</span>
</div>


</body>
</html>

