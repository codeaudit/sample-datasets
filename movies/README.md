Movies Sample Dataset
=====================

This sample dataset contains a small subset of the data behind the [Moogi](http://moogi.co) movie search engine.   

There are two version of this sample dataset.
* The "large-dataset" contains information on about 7300 movies and about 20000 people.
* The "small-dataset" contains information on about 1700 movies and about 5300 people.

After downloading the files and starting the MindmapsDB engine, the .gql files must be loaded into the engine in a specific order. 

_Notice that this can take easily take more than 30 minutes for the large dataset, depending on your computer._

First, the schema file must be loaded. Start the MindmapsDB engine and run the following command into your favourite shell:

```
/PATH/TO/graql.sh -f /PATH/TO/schema.gql
```

After that, the data has to be loaded:

```
/PATH/TO/graql.sh -b /PATH/TO/movie-data.gql
```

_Please notice that the two commands are different!_

In order to check the status of loading the data, you can open a new terminal, navigate to the `logs` directory in your MindmapsDB installation, and run the command:

```
tail -f mindmaps.log
```


If everything went well, you will be able to query your new dataset.

```
match $x isa person, has name $a; select $a;
```

<!--Removed screengrab as graql query no longer works.-->

