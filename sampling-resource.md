# GIT Sampling Resource
There is a resource designed to ease the process of sampling repositories or developers in Git. The resource is designed to allow users to perform basic restrictions then return a list of developers/repositories that fit the selected criteria. The resource uses the metadata collections described in described in this paper `http://arxiv.org/abs/2008.03439`. This API is in development and will have all the options listed in the above paper for researchers to perform sampling. 

# Available Sampling
### Timeframe Sampling
The API allows users to perform sampling using the active timeframe of an author/project. If the given timeframe is between the start and end date of an author/project it is counted. The timeframe of the Git object is based on the first and last commit time. 

### Language Sampling
The API allows users to perform sampling based on the languages used by the author/project. If the given language is one of many languages the author/project used it is counted. The language information is based off the file extensions associated with each file related to the given Git object. 

### File Sampling
The API allows users to perform sampling based on the total number of files related to the author/project. It is possible to sample based on the total number of any language file contained within the resource. If the user wants to sample projects that have 50+ python files it is possible. It is also possible to restrict based on the total number of files assosicated with the author/project.

### Data Storage/Retrieval
The data is stored within a MongoDB server, thus queries may take time to retrieve all the associated data. When the sampling is finished data is returned in JSON format.

### Restrictions
This sampling resource has some restrictions to what is possible. For more information on restrictions to the timeframe/language/file information see the above paper. 

![Image of Yaktocat](https://github.com/atutko2/msr-challenge/blob/master/Sampling%20Resource.png)
