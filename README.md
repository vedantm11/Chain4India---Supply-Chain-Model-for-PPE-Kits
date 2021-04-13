## Project Description

Substandard Quality Medical Equipment ( Masks and PPE kits) are manufactured and sold in the market at very cheap prices that are not safe. When these equipment reach hospitals they have to be Of Good Quality and Certified as they may hurt Patients As Well As Doctors and Hospital reputations. But it is difficult for hospitals to track i.e ->Where they were manufactured , How did it get there? ( problem of traceability )
->Is it Good Quality Medical Equipment? ( problem of Trust )
->Am I buying the equipment at an appropriate price ? ( Transparency )

We are providing a Blockchain based solution using Hyperledger Sawtooth Platform. We will be able to establish a network between multiple nodes i.e. distributed ledger using Hyperledger Sawtooth Platform.

## Video
https://drive.google.com/file/d/10i2ANKeOK4_X1tXVJqlB94gqu4KZKW6C/view?usp=sharing

## Presentation
https://he-s3.s3.ap-southeast-1.amazonaws.com/media/sprint/rakathon-2021/team/984273/cb0d4c1rakathon.pptx

## Demo
https://vibrant-heyrovsky-5625d7.netlify.app/chain4india.html


![Hyperledger Sawtooth](images/sawtooth_logo_light_blue-small.png)


## Contents

- [Components](#components)
- [Usage](#usage)
  - [Start Up](#start-up)
  - [Configuring API Keys and Secrets](#configuring-api-keys-and-secrets)
- [License](#license)

## Components

Running alongside the core components from Hyperledger Sawtooth, Supply Chain
includes a number of elements customizing the blockchain and user interaction
with it:

- a **transaction processor** which handles Supply Chain transaction logic
- a **server** which provides an HTTP/JSON API for Supply Chain actions
- a **ledger sync** which syncs blockchain data to a local database
- a **shell** container with the dependencies to run any commands and scripts


## Usage

This project utilizes [Docker](https://www.docker.com/what-docker) to simplify
dependencies and deployment. After cloning this repo, follow the instructions
specific to your OS to install and run whatever components are required to use
`docker` and `docker-compose` from your command line. This is only dependency
required to run Supply Chain components.

### Start Up

- The Supply Chain REST API will be at **http://localhost:8020**
- Hospital Client will be at **http://localhost:8026**
- Manufacturer Client will be at **http://localhost:8021**
- Certifying Client will be at **http://localhost:8025**
- RethinkDB's admin panel will be available at **http://localhost:8023**
- Sawtooth's blockchain REST API will be available at **http://localhost:8024**



### Configuring API Keys and Secrets

While the Server runs out of the box with sensible defaults, there are a number
of secrets and API keys which will not be secure unless set explicitly. While
this is fine for demo purposes, any actual deployment set the following
properties:

- **JWT_SECRET**: can be any random string
- **PRIVATE_KEY**: must be 64 random hexadecimal characters
- **MAPS_API_KEY**: provided by [Google Maps](https://developers.google.com/maps/documentation/javascript/get-api-key)

These properties can be set one of two ways, through an environment variable,
or (preferably) by creating a file named `config.json` file in the `server/`
directory. A file named `config.json.example` is provided which should provide
a template to follow.



## License of Hyperledger Sawtooth 

Hyperledger Sawtooth software is licensed under the
[Apache License Version 2.0](LICENSE) software license.

Hyperledger Sawtooth Supply Chain documentation in the [docs](docs)
subdirectory is licensed under a Creative Commons Attribution 4.0 International
License.  You may obtain a copy of the license at:
http://creativecommons.org/licenses/by/4.0/.

![Open Source Award Badge](images/rookies16-small.png)
