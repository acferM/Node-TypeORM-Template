# Node + TypeORM Template

## Ready to code 😃
this project has:
- tsconfig.json,
- prettier.config.js,
- ormconfig.json
- .eslintrc.json,
- .eslintignore
- .editorconfig

all already configurated

# How to use it 😤
all you have to do is:

1. on your terminal clone this repository and acess it using:
```bash
git clone https://github.com/acferM/NodeTemplate.git
cd NodeTemplate
yarn
```

2. start code on the files inside src/

3. to execute the in dev mode, on your terminal run:
```bash
yarn dev:server
```

4. to build the project, on your terminal run:
```bash
yarn build
```

# Package.json Scripts 📦
in your package.json files you will find a few more scripts, these scripts use the TypeORM CLI to manage your database

#### 1. typeorm:create-mi --> creates a migration wich name you put in the end of the command:
```bash
yarn typeorm:create-mi YouMigrationNameHere
```

#### 2. typeorm:run-mi --> executes the "up" method of all the new migrations
```bash
yarn typeorm:run-mi
```

#### 3. typeorm:revert-mi --> executes the "down" method of all the new migrations
```bash
yarn typeorm:revert-mi
```

#### 4. typeorm:show-mi --> show all the migrations that have been executed
```bash
yarn typeorm:show-mi
```

# Configs ⚙

## Eslint:
this is the content of the .eslintrc.json:

```json
{
  "env": {
      "es2020": true,
      "node": true
  },
  "extends": [
      "airbnb-base",
      "plugin:@typescript-eslint/recommended",
      "prettier/@typescript-eslint",
      "plugin:prettier/recommended"
  ],
  "parser": "@typescript-eslint/parser",
  "parserOptions": {
      "ecmaVersion": 2018,
      "sourceType": "module"
  },
  "plugins": [
      "@typescript-eslint",
      "prettier"
  ],
  "rules": {
     "import/extensions": [
      "error",
      "ignorePackages",
      {
        "ts": "never"
      }
    ],
    "prettier/prettier": "error",
    "class-methods-use-this": "off"
  },
  "settings": {
    "import/resolver": {
      "typescript": {}
    }
  }
}
```

and this is the .eslintignore content

```json
/*.js
node_modules
dist
```

## Prettier
this is the content of the prettier.config.js

```JavaScript
module.exports = {
  singleQuote: true,
  trailingComma: 'all',
  arrowParens: 'avoid',
}
```

## EditorConfig
this is the content of the .editorconfig

```json
root = true

[*]
end_of_line = lf
indent_style = space
indent_size = 2
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true
```

## TypeScript
this is the content of the tsconfig.json

```json
{
  "compilerOptions": {
    /* Visit https://aka.ms/tsconfig.json to read more about this file */

    /* Basic Options */
    // "incremental": true,                   /* Enable incremental compilation */
    "target": "es5",                          /* Specify ECMAScript target version: 'ES3' (default), 'ES5', 'ES2015', 'ES2016', 'ES2017', 'ES2018', 'ES2019', 'ES2020', or 'ESNEXT'. */
    "module": "commonjs",                     /* Specify module code generation: 'none', 'commonjs', 'amd', 'system', 'umd', 'es2015', 'es2020', or 'ESNext'. */
    // "lib": [],                             /* Specify library files to be included in the compilation. */
    // "allowJs": true,                       /* Allow javascript files to be compiled. */
    // "checkJs": true,                       /* Report errors in .js files. */
    // "jsx": "preserve",                     /* Specify JSX code generation: 'preserve', 'react-native', or 'react'. */
    // "declaration": true,                   /* Generates corresponding '.d.ts' file. */
    // "declarationMap": true,                /* Generates a sourcemap for each corresponding '.d.ts' file. */
    // "sourceMap": true,                     /* Generates corresponding '.map' file. */
    // "outFile": "./",                       /* Concatenate and emit output to single file. */
    "outDir": "./dist",                        /* Redirect output structure to the directory. */
    "rootDir": "./src",                       /* Specify the root directory of input files. Use to control the output directory structure with --outDir. */
    // "composite": true,                     /* Enable project compilation */
    // "tsBuildInfoFile": "./",               /* Specify file to store incremental compilation information */
    // "removeComments": true,                /* Do not emit comments to output. */
    // "noEmit": true,                        /* Do not emit outputs. */
    // "importHelpers": true,                 /* Import emit helpers from 'tslib'. */
    // "downlevelIteration": true,            /* Provide full support for iterables in 'for-of', spread, and destructuring when targeting 'ES5' or 'ES3'. */
    // "isolatedModules": true,               /* Transpile each file as a separate module (similar to 'ts.transpileModule'). */

    /* Strict Type-Checking Options */
    "strict": true,                           /* Enable all strict type-checking options. */
    // "noImplicitAny": true,                 /* Raise error on expressions and declarations with an implied 'any' type. */
    // "strictNullChecks": true,              /* Enable strict null checks. */
    // "strictFunctionTypes": true,           /* Enable strict checking of function types. */
    // "strictBindCallApply": true,           /* Enable strict 'bind', 'call', and 'apply' methods on functions. */
    "strictPropertyInitialization": false,  /* Enable strict checking of property initialization in classes. */
    // "noImplicitThis": true,                /* Raise error on 'this' expressions with an implied 'any' type. */
    // "alwaysStrict": true,                  /* Parse in strict mode and emit "use strict" for each source file. */

    /* Additional Checks */
    // "noUnusedLocals": true,                /* Report errors on unused locals. */
    // "noUnusedParameters": true,            /* Report errors on unused parameters. */
    // "noImplicitReturns": true,             /* Report error when not all code paths in function return a value. */
    // "noFallthroughCasesInSwitch": true,    /* Report errors for fallthrough cases in switch statement. */

    /* Module Resolution Options */
    // "moduleResolution": "node",            /* Specify module resolution strategy: 'node' (Node.js) or 'classic' (TypeScript pre-1.6). */
    // "baseUrl": "./",                       /* Base directory to resolve non-absolute module names. */
    // "paths": {},                           /* A series of entries which re-map imports to lookup locations relative to the 'baseUrl'. */
    // "rootDirs": [],                        /* List of root folders whose combined content represents the structure of the project at runtime. */
    // "typeRoots": [],                       /* List of folders to include type definitions from. */
    // "types": [],                           /* Type declaration files to be included in compilation. */
    // "allowSyntheticDefaultImports": true,  /* Allow default imports from modules with no default export. This does not affect code emit, just typechecking. */
    "esModuleInterop": true,                  /* Enables emit interoperability between CommonJS and ES Modules via creation of namespace objects for all imports. Implies 'allowSyntheticDefaultImports'. */
    // "preserveSymlinks": true,              /* Do not resolve the real path of symlinks. */
    // "allowUmdGlobalAccess": true,          /* Allow accessing UMD globals from modules. */

    /* Source Map Options */
    // "sourceRoot": "",                      /* Specify the location where debugger should locate TypeScript files instead of source locations. */
    // "mapRoot": "",                         /* Specify the location where debugger should locate map files instead of generated locations. */
    // "inlineSourceMap": true,               /* Emit a single file with source maps instead of having a separate file. */
    // "inlineSources": true,                 /* Emit the source alongside the sourcemaps within a single file; requires '--inlineSourceMap' or '--sourceMap' to be set. */

    /* Experimental Options */
    "experimentalDecorators": true,        /* Enables experimental support for ES7 decorators. */
    "emitDecoratorMetadata": true,         /* Enables experimental support for emitting type metadata for decorators. */

    /* Advanced Options */
    "skipLibCheck": true,                     /* Skip type checking of declaration files. */
    "forceConsistentCasingInFileNames": true  /* Disallow inconsistently-cased references to the same file. */
  }
}
```

## TypeORM
this is the content of the ormconfig.json
```json
{
  "type": "", // <-- your database type EX: postgres
  "host": "localhost", // <-- where is your connection made EX: localhost:3333
  "port": 0, // <-- port used by your computer to connect it to the docker container
  "username": "", // <-- username of your docker container
  "password": "", // <-- password choosed by you on the creation of the docker container
  "database": "", // <-- database name
  "entities": [
    "./src/models/*.ts" // <-- path to the entities paste
  ],
  "migrations": [
    "./src/database/migrations/*.ts" // <-- path to the migrations paste
  ],
  "cli": {
    "migrationsDir": "./src/database/migrations" // <-- path to the migrations paste (helps de typeORM cli)
  }
}
```

# Why TypeORM ? 🤔

#### 1. The TypeORM uses the ORM (Object Realational Mapping) wich makes the creation of a SOLID based API **MUCH** easier because of it's own repository and easy way to make models e make relations between models.

#### 2. TypeORM is very easy to connect with a DB using the ormconfig.json.

#### 3. TypeORM uses migrations wich makes team work more organized.

#### 4. TypeORM uses Knex.js behind the scenes wich makes possible to write DB queries using JS, with that we can write the same query an use it in **ALL** the databases.


# Documentation 📄

## [NodeJS](https://nodejs.org/en/docs/)

## [Express.js](https://expressjs.com/)

## [TypesScript](https://www.typescriptlang.org/docs/home.html)

## [TypeORM](https://typeorm.io/#/)

## [Docker](https://docs.docker.com/)

## [EditorConfig](https://editorconfig.org/#overview)

## [Prettier](https://prettier.io/docs/en/index.html)

## [Eslint](https://eslint.org/)
