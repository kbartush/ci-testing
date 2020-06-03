# CI Testing
[![CircleCI](https://circleci.com/gh/kbartush/ci-testing.svg?style=svg)](https://circleci.com/gh/kbartush/ci-testing)

This is a project for testing CI pipelines. It's a fun project.

      - publish-latest-rs:
          requires:
            - test
            - test-rs
          filters:
            branches:
              only: /release\/v([0-9]+)\.([0-9]+)\.([0-9]+)$/
      - publish-latest:
          requires:
            - publish-latest-rs
          filters:
            branches:
              only: /release\/v([0-9]+)\.([0-9]+)\.([0-9]+)$/
