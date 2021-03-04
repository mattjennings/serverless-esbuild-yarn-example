Steps:

- run `yarn` from root
- run `serverless deploy --noDeploy` within the `external` folder
- notice that it says "no external modules needed"
- clone `https://github.com/mattjennings/serverless-esbuild.git` somewhere and checkout to `support-yarn-workspaces` branch
  - build it and set up the link (`yarn && yarn build && yarn link`)
- link to serverless-esbuild in the `external` folder (`yarn link serverless-build`)
- run `serverless deploy --noDeploy` again
- the external modules are correclty detected and packaged
