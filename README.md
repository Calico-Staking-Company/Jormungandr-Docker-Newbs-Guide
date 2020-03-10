# Jormungandr Docker for Newbs Guide 

Newbs guide for setting up Jormungandr on a Docker Swarm. Much thanks to Mark Stopka at 2nd Layer, without whom this guide would be useless. Check out his work here! https://github.com/2nd-Layer/ and his Cardano Node/Jormungandr Docker project here https://github.com/2nd-Layer/docker-hub-cardano-images . Thank you so much for the help Mark!

## Getting Started

In this guide, you will set up a Docker Swarm with a single node for Jormungandr. It is set to auto-restart if anything fails, and we will go into how to handle your node-secret.yaml file with Docker Secrets. We will be setting up Ansible to deploy this easily with a target deploy time of three minutes once you are up to speed!

This guide assumes you have little to no familiarity with Docker, but if you do, this guide will be even easier and will explain how to configure the node and generate the appropriate certificates to start the node as a slot leader. We will also go over the pull request to make your staking pool official!

Later on, we will go over how to make Ansible do a bulk of the deployment work, with the target of bringing deployment time three minutes or so (if you have the pool already set up).

### Prerequisites

type stuff here

```
Give examples
```

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Cameron McDougle** - *Initial work* - [SeaWolfos](https://github.com/SeaWolfos)
* **Tedd Johnson** - *Initial work* - [Jawnz](https://github.com/JawnZ)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

Much thanks to Mark Stopka at 2nd Layer https://github.com/2nd-Layer/ . We relied heavily on his Docker Swarm setup at https://github.com/2nd-Layer/docker-hub-cardano-images . He also helped us out with questions we had!

Thanks to * **Billie Thompson** - *Readme Template* - [PurpleBooth](https://github.com/PurpleBooth)
for writing the README-Template.md file used here. 
