# Udagram Pipeline

![Pipeline](pipeline.drawio)

## Continuous Integration

#### GitHub

The developers commit and push their code to the GitHub repository which is linked to the CircleCI platform.
GitHub triggers the CircleCI platform when code is pushed to the repository.

#### CircleCI

CircleCI reads the `.circleci/config.yml` file which tells the service what has to be done. In the case of Udagram,
there are 2 jobs (build & deploy) to be run by CircleCI.

- **build**:Install node,elastic beanstalk and checkout code then Install Front-End and API Dependencies
  Finally build the frontend app and the backend API
- **deploy**:Install node,elastic beanstalk aws and checkout code then run `deploy` script
