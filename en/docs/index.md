<div class="homePage">
    <div class="section01">
        <div class="leftContent">
            <div class="about-homes">
                <div>
                    <p><b>WSO2 Observability Solution</b> provides a single place to monitor and analyze WSO2 integration products, whether it's a simple two instance cluster or a distributed micro-services style deployment with multiple Micro Integrator and Ballerina deployments.</p> 
                    <p>It contains built-in dashboards for administrators, service owners, and integration developers to visually inspect the behavior of services and integrations. In addition, it is possible to extend the capabilities of the observability solution by creating custom dashboards or by securely accessing observability data via the underlying APIs.</p>
                    <div class="linkSet2" onclick="location.href='{{base_path}}/get-started/quick-start-guide';">
                        <a href="get-started/quick-start-guide"><h3>Quick Start Guide</h3></a>
                        <p>
                            Get started by deploying the observability solution and samples in your local computer.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="section02">
        <div class="rightContent">
                <div class="about-home">
                    <div  style="text-align:center">
                        <a href="{{base_path}}/assets/img/introduction/central-loc.jpeg"><img src="{{base_path}}/assets/img/introduction/central-loc.jpeg" alt="low-code" width="60%" style="padding-top: 60px" ></a>
                    </div>
                    <div>
                        <h3>Collect analytics data on all integrations</h3>
                        <p>
                            With a simple configuration, all WSO2 integration deployments can publish analytics data to the Observability Solution. This data covers all integrations including APIs, GraphQL services, Websocket interactions, and messaging transactions.
                        </p>
                    </div>
                </div>
        </div>
    </div>
     <div class="section02">
        <div class="leftContent">
                <div class="about-home">
                    <div>
                        <h3>Analyze all logs from a single portal</h3>
                        <p>
                            Production environments usually have multiple clusters with multiple components in each cluster. In such situaions, it is crucial to access logs of all components from a single place and immediately identify errors.
                        </p>
                        <p>
                            Observability Solution collects logs from all integrations in the environment and extract relavent information from logs. Users can view all logs from a single dashboard and filter and drill-down on details as necessary.
                        </p>
                    </div>
                    <div  style="text-align:right">
                        <a href="{{base_path}}/assets/img/introduction/logs-dashboard.png"><img src="{{base_path}}/assets/img/introduction/logs-dashboard.png" alt="AI" width="90%" style="padding-top: 60px; padding-right: 50px" ></a>
                    </div>
                </div>
        </div>
    </div>
    <div class="section02">
        <div class="rightContent">
                <div class="about-home">
                    <div  style="text-align:left">
                        <a href="{{base_path}}/assets/img/introduction/metrics-dashboard.png"><img src="{{base_path}}/assets/img/introduction/metrics-dashboard.png" alt="low-code" width="90%" style="padding-top: 60px" ></a>
                    </div>
                    <div>
                        <h3>Get insights on integrations</h3>
                        <p>
                            Observability Solution captures data on request counts, failed messages, and response times on all integrations across the environment. Built-in dashboards provide insights derived from this data allowing users analyze the performance of thier integrations for desired time periods.
                        </p>
                    </div>
                </div>
        </div>
    </div>
    <div class="section02">
        <div class="leftContent">
                <div class="about-home">
                    <div>
                        <h3>View message flows across all components</h3>
                        <p>
                            Micro services applications have multiple services interacting with each other. It is important to track message flows across all services in order to get a holistic understanding about such systems and to quickly identify component affecting the overall user experience. 
                        </p>
                        <p>
                            Observability solution captures tracing data from message flows across the environment, and provides dashboards to view service interactions and to drill down into individual message flows.
                        </p>
                    </div>
                    <div  style="text-align:right">
                        <a href="{{base_path}}/assets/img/introduction/trace-dashboard.png"><img src="{{base_path}}/assets/img/introduction/trace-dashboard.png" alt="ballerina" width="90%" style="padding-top: 60px" ></a>
                    </div>
                </div>
        </div>
    </div>
</div>
{% raw %}
<style>
.md-sidebar.md-sidebar--primary {
    display: none;
}
.md-sidebar.md-sidebar--secondary{
    display: none;
}
.section02 {
    display: flex;
    justify-content: space-between;
}
header.md-header .md-header__button:not([hidden]) {
    /* display: none; */
}
.about-home {
    display: flex;
}
.about-home div:first-child {
    width: 50%;
    padding-top: 20px;
}
.about-home div:nth-child(2) {
    width: 50%;
}
@media screen and (max-width: 76.1875em) {
    .md-sidebar.md-sidebar--primary {
        display: block;
    }
}
@media screen and (max-width: 945px) {
    .about-home div:first-child {
        width: 100%;
    }
    .about-home div:nth-child(2) {
        width: 100%;
    }
    .about-home {
        flex-direction: column;
    }
    .md-typeset a {
        background-position-x: left;
    }
    .download-btn-wrapper {
        display: block;
        text-align: center;
    }
}
.md-typeset h1{
    visibility: hidden;
    margin-bottom: 0;
}
.md-search-result__article.md-typeset h1{
    visibility: visible;
}
</style>
{% endraw %}