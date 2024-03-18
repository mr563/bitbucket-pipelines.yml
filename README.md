image:
name:node:18
# Add a code linting step to check your app’s code for common errors:
pipelines:
  default:
    - step:
        name: Check Code linting
        script:
          - npm install
          - npm install --global @forge/cli
          - forge settings set usage-analytics true
          - forge lint
        caches:
          - node
