Running a basic HDFS operation

http://hadoop.apache.org/common/docs/current/quickstart.html

Configure your hadoop-0.20.1/conf/hdfs-site.xml

<?xml version="1.0"?>
<?xml-stylesheet type="text/xsl" href="configuration.xsl"?>

<!-- Put site-specific property overrides in this file. -->

<configuration>
  <!-- Matthew 2010-01-13 -->
  <property>
         <name>fs.default.name</name>
         <value>localhost:9000</value>
  </property>
  <property>
         <name>mapred.job.tracker</name>
         <value>localhost:9001</value>
  </property>
  <property>
        <name>dfs.replication</name>
        <value>1</value>
  </property>
</configuration>



Format the HDFS filesystem:
hadoop namenode -format