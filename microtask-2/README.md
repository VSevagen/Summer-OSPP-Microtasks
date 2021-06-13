## Microtask-2

Learn about setup.cfg & projects.json and set up data collection for the GrimoireLab project using SirMordred. Feel free to choose any backend and the projects.

## Steps

1. Install ElasticSearch(6.8.6), Kibiter(6.8.6) and MariaDB database. Installed MariaDB seperately and used the docker-compose file for ElasticSearch and Kibiter.
2. Cloned all the GrimoireLab repos using this [script](https://gist.github.com/vchrombie/4403193198cd79e7ee0079259311f6e8)
3. Installed all the dependencies through the Project Interpreter and set up the project structure according to the tutorial.
4. Open PyCharm and go to directory where <code>docker-compose.yml</code> is.
5. Run <code>docker-compose up</code> to run Kibiter and ElasticSearch
6. Run <code>micro.py --raw --enrich --cfg ./setup.cfg --backends git</code> as shown in the tutorial
7. Run <code>micro.py --panels --cfg ./setup.cfg</code>

## What is setup.cfg ?

setup.cfg is the configuration file that hold the processese related to data collection, data enrichment, storage of SortingHat creds
and instances of the raw and enriched ElasticSearch data.

## What is projects.json ?

projects.json is the JSON file responsible for the data in the dashboard. It is where a user can list out the platforms from
where, according to the data, a visualization of some sort will be displayed.

## Issues faced

1. Run into the empty index issue. Solved it by disabling latest_items as shown in the Getting-Started file
2. Ran into [Issue#274](https://github.com/chaoss/grimoirelab/issues/274) and used the solution provided.

Here is a demo

![GrimoireLab Demo](GrimoireLab.gif)
