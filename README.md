# HIV Support

[![GitHub contributors][ico-contributors]][link-contributors]
[![GitHub last commit][ico-last-commit]][link-last-commit]
[![License: MPL 2.0][ico-license]][link-license]

HIV Support is a case manager dedicated to support CSOs who receive helprequests from refugees with HIV who seek help to continue treatment and toaccess other services relevant for their condition.

[See the project live][link-production]

[Contributing](#contributing) | [Built with](#built-with) | [Deployment](#deployment) | [Feedback](#feedback) | [License](#license) | [About Commit Global](#about-commit-global)

## Contributing

This project is built by an amazing team of civic technologists and amazing volunteers and you can be one of them! Here's a list of ways in [which you can contribute to this project][link-contributing]. If you want to make any change to this repository, please **make a fork first**.

Help us out by testing this project. If you see something that doesn't quite work the way you expect it to, open an Issue. Make sure to describe what you _expect to happen_ and _what is actually happening_ in detail.

If you would like to suggest new functionality, open an Issue and mark it as a __[Feature request]__. Please be specific about why you think this functionality will be of use. If you can, please include some visual description of what you would like the UI to look like, if you are suggesting new UI elements.

## Built With

### Programming languages

Python 3.9
### Backend framework

Django 3.2

### Package managers

pip

### Database technology & provider

PostgreSQL

## Deployment

```sh
# 1. Clone the repo
git clone https://github.com/commitglobal/hiv-support.git

# 2. Copy the environment variables file
cp .env.prod .env

# 3. Build the containers
docker-compose build

# 4. Start the application
docker-compose up -d
```

### Environment variables

The `.env` files contain variables required to start the services and initialize them.

- `ENVIRONMENT` - [`test`|`development`|`production`] sets the type of deployment (default `production`)
- `RUN_MIGRATION` - [`yes`|`no`] run django migrations when you start the app (default `yes`)
- `RUN_COMPILEMESSAGES` - [`yes`|`no`] compile i18n messages when you first start the app (default `yes`)
- `RUN_SEED_DATA` - [`yes`|`no`] load the data from the `fixtures/` folders (default `no`)
- `RUN_COLLECT_STATIC` - [`yes`|`no`] collects static data like images/fonts (default `yes` - has no effect if `ENVIRONMENT != production`)
- `RUN_DEV_SERVER` - [`yes`|`no`] starts the app in development mode with a more comprehensive debugging toolbox (default `no`)
- `DATABASE_URL` - the URL Django will use to connect to the database (should be changed if you're not running through Docker)
- `SECRET_KEY` - the secret key Django will use to encrypt data (should be changed if you're not running through Docker)

## Feedback

* Request a new feature on GitHub.
* Vote for popular feature requests.
* File a bug in GitHub Issues.
* Email us with other feedback contact@code4.ro

## License

This project is licensed under the MPL 2.0 License - see the [LICENSE](LICENSE) file for details

## About Commit Global

The team behind Commit Global has a robust and celebrated track record in the tech for social good field since 2015. We have built the fastest growing organization in the space, Code for Romania and set it up as a model of good practices on how to design and build technology that helps at scale. Our tools have served governments, UN agencies and large and small CSOs during crisis and peace time. Most recently we have built, deployed and maintained a first of its kind humanitarian ecosystem in support of refugees fleeing from Ukraine, ensuring their safe and uninterrupted access to information, healthcare and services, while equipping NGOs with the tools they need to be more effective.

All throughout our activity we have been one of the champions of cooperation and co-creation in the the civic tech field, constantly investing efforts and resources in working with and supporting the work of similar organizations around the world. As part of these efforts we created, curated and hosted the largest civic tech strategic event in history, the 2018 Code for All Global Summit: a 4 days offline event where hundreds of delegates from all continents exchanged ideas and digital solutions for the benefit of humanity.

Find more details on https://www.commitglobal.org/en


[ico-contributors]: https://img.shields.io/github/contributors/commitglobal/hiv-support.svg?style=for-the-badge
[ico-last-commit]: https://img.shields.io/github/last-commit/commitglobal/hiv-support.svg?style=for-the-badge
[ico-license]: https://img.shields.io/badge/license-MPL%202.0-brightgreen.svg?style=for-the-badge

[link-contributors]: https://github.com/commitglobal/hiv-support/graphs/contributors
[link-last-commit]: https://github.com/commitglobal/hiv-support/commits/main
[link-license]: https://opensource.org/licenses/MPL-2.0
[link-contributing]: https://github.com/code4romania/.github/blob/main/CONTRIBUTING.md

[link-production]: https://app.consilierehiv.ro
