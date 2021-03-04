Steps:

- run `yarn` from root
- try running `serverless deploy --noDeploy` within the `externally`
- notice that it says "no external modules needed"
- clone `https://github.com/mattjennings/serverless-esbuild.git` and checkout to `support-yarn-workspaces` branch
  - build it and set up the link (`yarn && yarn build && yarn link`)
- link to serverless-esbuild in the `external` folder (`yarn link serverless-build`)
- run `serverless deploy --noDeploy` again
- the external modules are correclty detected and packaged
