# tags-user
> Apibuilder api specification for .

One to two paragraph statement about your product and what it does.

![](header.png)

## Why
1. This project structure and tooling: 
    1. allows api definitions to have a life cycle independent of clients or implementations
    1. encourages Api First Engineering
    1. automates common tasks associated with using apibuilder 

1. Provides an api definition for the tags-user interface that can 
be validated and used to generate high quality clients, implementations, 
mocks, openapi docs, databases, cloudformation, ect using any 
apibuilder.io generator public or custom. This definition can also be 
subjected to public and or custom validation to help enforce API standards. 

## Installation

## Usage example

## Development setup

You will need to install and configure [apibuilder-cli](https://github.com/apicollective/apibuilder-cli) 

### Project Types

#### API Definition Projects

Api Definition projects are used purely to define an API so that other 
projects can refrence it and generate clients / implementations.This type 
of project is recomemnded also whenever you may want to share the model 
with other api's. As an example If I were to define an api for health checks 
one would want to make sure that api is consistent across all services. 

#### API Client Projects

Api Client projects use code generaton only, although it is common to add an 
api definition if you are collated api functionality from other api definitions. 
This allows you to track and evolve collated api's independently and use a 
collated version for generating clients / implementations.  
 

### File System
```
├── .apibuilder  - Contains Apibuilder configuration for this project
│   └── config - Apibuilder generation configuration.
├── .gitignore
├── README.md
├── api.json - Contains Apibuilder API definition for this project.
├── bin
│   ├── Functions.sh - Generic bash helper functions
│   ├── Header.sh -
│   ├── generate.sh - Runs the Apibuilder generation defined in the Apibuilder generation configuration.
│   ├── push.sh - Pushes the Apibuilder API definition to apibuilder.io using the version defined in project-config.yaml
│   ├── pushAndGenerate.sh - Convience command, runs push.sh and generate.sh
│   └── pushLatest.sh - Pushes the current Apibuilder API definition with the version string 'latest'
└── project-config.yaml - Defines basic properties for this project like Organization, Name, and Version
```

### Configuring Generation

Generation configuration is in  
```
├── .apibuilder  - Contains Apibuilder configuration for this project
│   └── config - Apibuilder generation configuration.
```
This is a standard apibuilder-cli config file, details and syntax [here](https://github.com/apicollective/apibuilder-cli) .

#### Api Definition projects.
It is recomended that you generate only for testing to the
```
├── src 
```
directory, this directory should also be added to .gitignore to avoid commiting test code

#### Api Client projects.
It is recomended that you generate only for testing to the
```
├── src 
```
directory, this directory should also be added to .gitignore to avoid commiting test code







## Release History

* 0.0.1
    * Initial Project Commit
## Meta

## Contributing

1. Fork it (<https://github.com///fork>)
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request

