# Monorepo Turborepo Trial
>- Turborepo, developed by Vercel, is a powerful tool that makes managing monorepos easier by optimizing workflows, speeding up build times, and ensuring consistency across projects
>- Turborepo is a high-performance build system for JavaScript and TypeScript codebases. It is designed for scaling monorepos and also makes workflows in [single-package workspaces](https://turborepo.com/docs/guides/single-package-workspaces) faster, too.
>- The `name` field is important because it specifies the name of the workspace. This name is used to refer to this specific workspace when running scripts or defining dependencies between local workspaces.
>- Each package is its own workspace. They can have their own scripts, their own dependencies, and they can depend on each other.
>- Web app depends on our UI library, which is a workspace package, as indicated in the dependencies section.
We also have some `devDependencies`, such as `eslint-config` and `typescript-config`, which are listed in the `packages` folder

## Run Locally

Clone the project

```bash
  git clone https://github.com/andrt2607/monorepo-turborepo-trial.git
```

Go to the project directory

```bash
  cd monorepo-turborepo-trial
```

```js
//command init create turborepo
npx create-turbo@latest
```

```js
//command run project turborepo
npm run dev

//command run specific project
npm run dev --workspace web
npm run dev --workspace docs

// add dependency to specific project
npm install axios -D -w web //rest client
npm install graffle -D -w web //graphql client
```

## Notes
>    - node_modules => A shared folder for all the modules and packages used across all of your apps and packages
>    - packages => Contains different packages or libraries that are shared between your apps
>    - eslint-config => Shared ESLint configuration for your apps.
>    - typescript-config => Shared TypeScript configuration for your apps
>    - ui components => A React.js library to be shared between your apps


## Authors

- [@alifandarta](https://www.github.com/andrt2607)