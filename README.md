# webpack-encore-babel-issue

Installing and adding `@babel/plugin-proposal-decorators` to the plugin list make encore exit without building.

To recreate the issue:
1. Clone this git repository
2. Run `yarn install`
3. Then run `yarn encore` (or `npx encore dev --stats=verbose`)
4. Encore should say `Running webpack ...` and then exists without building
5. Now comment out line 53 in `webpack.config.js`
6. Run `yarn encore` (or `npx encore dev --stats=verbose`) again and now it does build but without `@babel/plugin-proposal-decorators`
