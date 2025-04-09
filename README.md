# Benchmarking Performance, Scalability and Resilience of Aerospike and Apache Cassandra - Data Set

This repo contains the associated raw benchmark results of the benchmarking study [TODO](TODO). 

The `benchmarkConfigurations` folder contains the JSON based benchmark scenarios as provided to the benchANT platform for the three benchmark cases:
- `performance`
  - `calibration`
  - `production` 
- `scale-out`
- `resilience`

While these benchmark scenarios can be directly applied to benchANT platform to repeat the benchmark runs, they also include all relevant parameters to reproduce the benchmarks without the benchANT platform. 

The `results` folder contains the raw result data for the three benchmark cases:
- `performance`
  - `calibration`
  - `production` 
- `scale-out`
- `resilience`

For more details on the methodology and the benchmark objectives please refer to the associated report.

Each raw result folder contains the data of a single run benchmark of one configuration. 

***

## Data Set Structure


In order to ensure full transparency and reproducibility,  each data folder contains benchmark configuration data,  performance data, monitoring data, cloud provider metadata, VM metadata and DBMS configuration data. The main metadata files are described below.  
 

***

### Benchmark Configuration Data

All configurable benchmark parameters are defined in the `evaluationScenario.json`.

The `benchANT_versions` contains the used versions of the benchANT software components to execute the benchmarks. 

The execution logs of the individual benchmark steps are contained in `airflowTaskInstanceDetails.json`. 

***

### Performance Data

The raw performance data output of the YCSB is contained in the `0_load.txt` for loading the initial data set and in the `0_run.txt` for the actual query phase. 

***

### Monitoring Data

The DBMS cluster and the benchmark instances are monitored with [Telegraf](https://github.com/influxdata/telegraf) and the data is stored in [InfluxDB](https://github.com/influxdata/influxdb). 

A full snapshot of the monitoring data of each run is contained in the  `influx_data.zip` file.



*** 

### Cloud Provider Metadata

The cloud provider metadata for the DBMS instances are available in the `dbms_data_resources.json` and for the YCSB benchmark deployment in the `benchmark_resources.json`. 


*** 

### VM Metadata

The VM metadata for the DBMS deployment is contained in the `dbms_data_hardware_facts.json` / `dbms_management_hardware_facts.json` and for the benchmark deployment in the `benchmark_hardware_facts.json`.  


*** 


## Contact

In case of questions or feedback on the data feel free to create an issue or reach out to info@benchant.com

