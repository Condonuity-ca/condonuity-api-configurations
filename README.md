# Introduction 
This is configuration repository for all condonuity project repos

# Getting Started
All services + servers will individually host their respective configurations across 3 environments - dev, staging and production 

# Build and Test
In order to build and run services on your local machine please do the following in each maven module run configuration:

(a) Set the -Dspring.profiles.active parameter to dev 
This should pick up all configurations based on the {application-name}-dev.yml properties file 

(b) Custom override local properties 
If you wish to custom override local properties i.e. not from the repo,
   - Create a local property file ex. {user-service-local.yml}; note the {location}
   - Copy the boilerplate properties from the user-service-dev.yml in this repository
   - Change + add attributes as required for local run ex. DB passwords etc.
   - Change the run configuration on local to include environment variable set as 
            spring.config.location={location}/{user-service-local.yml} 

# Contribute
For a new maven module to be added to parent project
    - Create a new folder in this repository for configuration
    - Name the property files as per the applciation name setting in the new module
        For ex. New module is to be created for insurance-service; add the spring.application.name=insurance-service in modules application.properties file
    - Name the cinfiguration files as {application-name}-{profile}.yml
