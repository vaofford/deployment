# Deployment
Deploys the general repository

[![Build Status](https://travis-ci.org/sanger-pathogens/deployment.svg?branch=master)](https://travis-ci.org/sanger-pathogens/deployment)   
[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-brightgreen.svg)](https://github.com/sanger-pathogens/deployment/blob/master/LICENSE)   

## Contents
  * [Introduction](#introduction)
  * [Installation](#installation)
    * [Required](#required)
    * [running the tests](#running-the-tests)
  * [Usage](#usage)
  * [License](#license)
  * [Feedback/Issues](#feedbackissues)

## Introduction
This application does:

1. Checkout a clean copy
2. Build the files
3. Run the tests
4. Build and install the documentation
5. Install the files

Its must be run from a machine with /software mounted on it so that java libraries are accessible, and to avoid permissions issues it needs to be run by pathdb.
```
ssh pathdb@pathinfo-test
```

## Installation
Deployment has the following dependencies:

### Required
* NaturalDocs
* Getopt::Long
* Net::SCP
* Git::Repository

If you encounter an issue when installing deployment please contact your local system administrator. If you encounter a bug please log it [here](https://github.com/sanger-pathogens/deployment/issues) or email us at path-help@sanger.ac.uk.

First install the dependencies, then clone the repo:
```
git clone https://github.com/sanger-pathogens/deployment.git
```

### running the tests
```
make test
```

## Usage
```
./deploy.pl -e test
```
or
```
./deploy.pl -e production
```  

## License
Deployment is free software, licensed under [GPLv3](https://github.com/sanger-pathogens/deployment/blob/master/LICENSE).

## Feedback/Issues
Please report any issues to the [issues page](https://github.com/sanger-pathogens/deployment/issues) or email path-help@sanger.ac.uk.
