# nmon

- [Visualizing nmon Files in ad-hoc Mode](../../integration/nmon/ad-hoc.md)
- [Deploy nmon](../../integration/nmon/deploy.md)
- [nmon File Streaming over Telnet](../../integration/nmon/file-streaming.md)
- [File Upload](../../integration/nmon/file-upload.md)
- [Format](../../integration/nmon/format.md)
- [Headers](../../integration/nmon/headers.md)
- [Parser](../../integration/nmon/parser.md)
- [Scheduled File Upload to ATSD](../../integration/nmon/scheduled-file-upload.md)
- [Sender Script](../../integration/nmon/sender-script.md)
- [SSH Tunnel Setup](../../integration/nmon/ssh-tunneling.md)

## Overview

Nmon is a system performance monitoring tool designed by [Nigel Griffiths at IBM](http://www.ibm.com/developerworks/aix/library/au-analyze_aix/), originally for AIX, and later ported to Linux.

To this day, nmon remains the preferred data collection daemon on AIX and is gaining traction with Linux administrators as well. Some of the advantages of nmon include:

-   Single binary, easy to install
-   Console and batch mode
-   Scheduled with cron
-   Collects granular statistics at specified interval
-   Collects output of key system commands
-   Compact data format

On AIX, nmon is pre-installed on AIX 5.3 and 6.1 and newer versions by default. On older AIX versions 4.1.5, 4.2, 4.3, 5.1, and 5.2, nmon can be installed manually.

In Linux, nmon is [open sourced under GPL license](https://github.com/axibase/nmon). It can be downloaded as an [executable binary](https://github.com/axibase/nmon/releases) or can becompiled from source. Supported distributions include Ubuntu, Debian, RHEL, CentOS, Fedora, SLES, and OpenSUSE.

The nmon file format is supported in Axibase Time Series Database natively. As a result, ATSD can be deployed as a centralized repository of nmon-sourced statistics and system commands collected from remote systems while providing access to [Visualization](http://axibase.com/products/axibase-time-series-database/visualization/ "Visualization"), [Alerting](../../rule-engine "Rule Engine"), and [Forecasting](http://axibase.com/products/axibase-time-series-database/forecasts/ "Forecasts") features.

[![](resources/widget-bar-2.png "widget bar 2")](http://axibase.com/products/axibase-time-series-database/visualization/widgets/)


## Installation steps

ATSD supports two ways of automated data ingestion from servers gathering nmon statistics:

-   [Scheduled upload](https://github.com/axibase/nmon#upload-hourly-files-to-atsd-with-wget) using wget, nc, or Unix pipes. Latency depends on the collection interval.
-   Streaming transmission of nmon snapshots as they are written into nmon output file using [sender script](sender-script.md). This method results in no latency; however, it requires more effort to implement.

nmon source code repository:
[https://github.com/axibase/nmon](https://github.com/axibase/nmon)


## Portals
![](resources/nmon-use-case-ATSD1.jpg "nmon use case ATSD")

[Live AIX nmon Portal](http://axibase.com/chartlab/b69e4fcd/3/)



![](resources/nmon-aix-portal-1500.png "nmon aix portal 1500")


[Live Linux nmon Portal ](http://axibase.com/chartlab/ac003f06)

![](resources/linux_nmon_portal.png "linux_nmon_portal")
