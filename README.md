# Axibase Time Series Database Documentation


* Installation
    * [Requirements](administration/requirements.md)
    * [Distributions](installation/#installation-guides)
	  * [Ubuntu/Debian (apt)](installation/ubuntu-debian-apt.md)
	  * [Ubuntu/Debian  (deb)](installation/ubuntu-debian-deb.md)
	  * [RedHat/CentOS (yum)](installation/redhat-centos-yum.md)
	  * [RedHat/CentOS (rpm)](installation/redhat-centos-rpm.md)
	  * [SUSE Linux Enterprise Server (rpm)](installation/sles-rpm.md)
	  * [VMware VM](installation/vmware-esxi-server-vsphere.md)
	  * [Oracle VirtualBox VM](installation/virtualbox.md)
	  * [Other](installation/other-distributions.md)
* [API](api)
    * [Data](api/data#overview)
      * Series: [query](api/data/series/query.md), [insert](api/data/series/insert.md), [csv insert](api/data/series/csv-insert.md), [url query](api/data/series/url-query.md)
      * Properties: [query](api/data/properties/query.md), [insert](api/data/properties/insert.md), [url query](api/data/properties/url-query.md), [type query](api/data/properties/type-query.md), [delete](api/data/properties/delete.md)
      * Messages: [query](api/data/messages/query.md), [insert](api/data/messages/insert.md), [statistics](api/data/messages/stats-query.md)
      * Alerts: [query](api/data/alerts/query.md), [update](api/data/alerts/update.md), [delete](api/data/alerts/delete.md), [history query](api/data/alerts/history-query.md)
    * [Meta](api/meta#overview)
      * Metrics: [list](api/meta/metric/list.md), [get](api/meta/metric/get.md), [update](api/meta/metric/update.md), [delete](api/meta/metric/delete.md), [creare/replace](api/meta/metric/create-or-replace.md), [series](api/meta/metric/series.md)
      * Entities: [list](api/meta/entity/list.md), [get](api/meta/entity/get.md), [update](api/meta/entity/update.md), [delete](api/meta/entity/delete.md), [creare/replace](api/meta/entity/create-or-replace.md), [metrics](api/meta/entity/metrics.md), [entity-groups](api/meta/entity/entity-groups.md), [property-types](api/meta/entity/property-types.md)
      * Entity Groups: [list](api/meta/entity-group/list.md), [get](api/meta/entity-group/get.md), [update](api/meta/entity-group/update.md), [delete](api/meta/entity-group/delete.md), [creare/replace](api/meta/entity-group/create-or-replace.md), [get-entities](api/meta/entity-group/get-entities.md), [add-entities](api/meta/entity-group/add-entities.md), [replace-entities](api/meta/entity-group/replace-entities.md), [delete-entities](api/meta/entity-group/delete-entities.md)
    * [Network](api/network#network-api)
      * [series](api/network/series.md)
      * [property](api/network/property.md)
      * [message](api/network/message.md)
      * [csv](api/network/csv.md)
      * [nmon](api/network/nmon.md)
	  * [command](api/network/nmon.md)
    * [SQL](api/sql#overview)  
		* [Syntax](api/sql#syntax)
		* [Interpolation](api/sql#interpolation)
		* [Grouping](api/sql#grouping)
		* [Partitioning](api/sql#partitioning)
		* [Ordering](api/sql#ordering)
		* [Joins](api/sql#joins)
		* [Examples](api/sql#examples)
* [API Clients](api#api-clients)
    * [R](https://github.com/axibase/atsd-api-r)
    * [PHP](https://github.com/axibase/atsd-api-php)
    * [Java](https://github.com/axibase/atsd-api-java)
    * [Python](https://github.com/axibase/atsd-api-python)
    * [Ruby](https://github.com/axibase/atsd-api-ruby)
    * [NodeJS](https://github.com/axibase/atsd-api-nodejs)
* Drivers
    * [JDBC](https://github.com/axibase/atsd-jdbc)
* Rule Engine
    * [Overview](rule-engine/rule-engine.md)
    * [Expression](rule-engine/expression.md)
    * [Functions](rule-engine/functions.md)
    * [Placeholders](rule-engine/placeholders.md)
    * [Email Action](rule-engine/email-action.md) 
* Integration
    * [ActiveMQ](integration/activemq#monitoring-activemq-with-atsd)
    * [Axibase Enterprise Reporter](integration/aer#atsd-adapter)
    * [IBM Tivoli Monitoring](integration/itm#ibm-tivoli-monitoring)
    * [Derby] (https://github.com/axibase/axibase-collector-docs/tree/master/jobs/examples/derby#overview)
    * [HP Openview](https://github.com/axibase/axibase-collector-docs/tree/master/jobs/examples/hp-openview#overview)
    * [Jetty](https://github.com/axibase/axibase-collector-docs/tree/master/jobs/examples/jetty#overview)
    * [JVM](https://github.com/axibase/axibase-collector-docs/tree/master/jobs/examples/jvm#overview)
    * [MySQL Server](https://github.com/axibase/axibase-collector-docs/tree/master/jobs/examples/mysql#overview)
    * [NGINX](https://github.com/axibase/axibase-collector-docs/tree/master/jobs/examples/nginx#overview)
    * [Oracle Enterprise Manager](https://github.com/axibase/axibase-collector-docs/tree/master/jobs/examples/oracle-enterprise-manager#overview)
    * [PostgreSQL](https://github.com/axibase/axibase-collector-docs/tree/master/jobs/examples/postgres#overview)
    * [Microsoft System Center Operations Manager](https://github.com/axibase/axibase-collector-docs/tree/master/jobs/examples/scom#overview)
    * [SolarWinds](https://github.com/axibase/axibase-collector-docs/tree/master/jobs/examples/solarwinds#overview)
    * [Tomcat Servlet Container](https://github.com/axibase/axibase-collector-docs/tree/master/jobs/examples/tomcat#overview)
    * [VMware](https://github.com/axibase/axibase-collector-docs/tree/master/jobs/examples/vmware#overview)
* [Administration](administration#administration)
    * [Deployment](administration/deployment.md)
    * [Setting up the Email Client](administration/setting-up-email-client.md)
    * [User Authentication](administration/user-authentiication.md)
    * [User Authorization](administration/user-authorization.md)
    * [Restarting](administration/restarting.md)
    * [Updating](administration/update.md)
    * [Uninstalling](administration/uninstalling.md)
    * [Migrate ATSD to Java 7](administration/migrate-to-java7.md)
    * [Network Settings](administration/networking-settings.md)
    * [Enabling Swap Space](administration/enabling-swap-space.md)
    * [Enabling Replication](administration/replication.md)
    * [Allocating Memory to components](administration/allocating-memory.md)
    * [Changing the Directory Where Data is Stored](administration/changing-data-directory.md)
    * [Editing Configuration Files](administration/editing-configuration-files.md)
    * [Logging](administration/logging.md)
    * [Metric Persistence Filter](administration/metric-persistence-filter.md)
    * [Entity Lookup](administration/entity-lookup.md)
    * [Restoring a corrupted zookeeper](administration/entity-lookup.md)
    * [Compaction](administration/compaction.md)
    * [Compaction Test](administration/compaction-test.md)
    * [Monitoring](administration/monitoring.md)