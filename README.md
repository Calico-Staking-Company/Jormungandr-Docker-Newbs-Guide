# Jormungandr Docker for Newbs Guide 

Newbs guide for setting up Jormungandr on a Docker Swarm. Much thanks to Mark Stopka at 2nd Layer, without whom this guide would be useless. Check out his work here! https://github.com/2nd-Layer/ and his Cardano Node/Jormungandr Docker project here https://github.com/2nd-Layer/docker-hub-cardano-images . Thank you so much for the help Mark!

## Getting Started

In this guide, you will set up a Docker Swarm with a single node for Jormungandr. It is set to auto-restart if anything fails, and we will go into how to handle your node-secret.yaml file with Docker Secrets. We will be setting up Ansible to deploy this easily with a target deploy time of three minutes once you are up to speed!

This guide assumes you have little to no familiarity with Docker, but if you do, this guide will be even easier and will explain how to configure the node and generate the appropriate certificates to start the node as a slot leader. We will also go over the pull request to make your staking pool official!

This is optional, but later on, we will go over how to make Ansible do a bulk of the deployment work, with the target of bringing deployment time three minutes or so (if you have the pool already set up).

If you have any questions, feel free to reach out!

### Prerequisites

To start off, you will need a server with enough RAM to run Jormunandr. We recommend 4-8GB. You can run whatever Linux distro you want, but we will be writing this up for Ubuntu. Digital Ocean works great, and if you're new, follow <this link> for a $100 free voucher. They also have great guides for setup <here>, <here>, and <here>.

You will also need to generate your pool certs. We're currently working on a guide to do this with ansible, so stay tuned. Otherwise, head over to the Jormungandr for Newbs Guide <here>.

## Setup Docker

Once you have your server set ip, install Docker.io:

```
apt install docker.io
```

## Set up directories


```
mkdir jormungandr 
mkdir jormungandr/conf 
cd jormungandr
```
## Add Docker permissions to your user

```
$ sudo groupadd docker
$ sudo usermod -aG docker $USER # change $USER for your username
```

## Configure Docker to start on boot

```
$ sudo systemctl enable docker
```

For more info on post-installation Docker setup, go <a href="https://docs.docker.com/install/linux/linux-postinstall/">here</a>. 


## Setting up your config files

Download your node-config.yaml file <a href="https://hydra.iohk.io/build/1523436/download/1/index.html">here</a> for v0.8.13. You're looking for the itn_rewards_v1 entry (unless you're going crazy and doing the nightly build or something). 

Then copy the Genesis Hash and put it in a file called genesis-hash.txt.

Find your pool-secret.yaml file. Put all three in the directory <>.

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
