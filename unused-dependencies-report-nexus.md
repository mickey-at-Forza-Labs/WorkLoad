# Unused Dependencies Report

Generated on March 31, 2026

This report was generated using `depcheck` to identify unused dependencies in each project within the Nexus monorepo.

## Root Project

### Unused Dependencies Pre-rework
None

### Unused Dependencies Pre-rework
- vitest


### Unused Dependencies After-rework
None

### Unused DevDependencies After-rework
- vitest

### Missing Dependencies
- globals
- @eslint/js
- typescript-eslint
- eslint-plugin-react
- @stylistic/eslint-plugin

## apps/dev_ops

### Unused Dependencies Pre-rework
- @aws-sdk/client-lambda
- @aws-sdk/client-redshift-data
- @aws-sdk/s3-request-presigner
- @aws-sdk/util-dynamodb
- all
- esbuild
- lodash
- aws-jwt-verify

### Unused Dependencies Pre-rework
- @eslint/js
- @stylistic/eslint-plugin
- eslint
- eslint-plugin-react
- tsx
- typescript-eslint

### Unused Dependencies After-rework
None

### Unused DevDependencies After-rework
- tsx


### Missing Dependencies
- @nasco/nexus-sdk
- uuid

## apps/nexus_backend

### Unused Dependencies Pre-rework
- @aws-sdk/client-cognito-identity-provider
- @aws-sdk/client-dynamodb
- @aws-sdk/client-lambda
- @aws-sdk/client-redshift-data
- @aws-sdk/s3-request-presigner
- @aws-sdk/util-dynamodb
- @nasco/nexus-backend
- aws-sdk
- cd

### Unused Dependencies Pre-rework
- @eslint/js
- @stylistic/eslint-plugin
- eslint
- eslint-plugin-react
- ts-node
- typescript
- typescript-eslint

### Unused Dependencies After-rework
None

### Unused DevDependencies After-rework
- typescript

### Missing Dependencies
- aws-lambda

## apps/nexus_frontend

### Unused Dependencies Pre-rework
- @codemirror/lang-javascript
- @codemirror/lang-json
- @dagrejs/dagre
- @date-io/dayjs
- @emotion/react
- @emotion/styled
- @mui/x-charts
- @mui/x-data-grid-generator
- @mui/x-date-pickers-pro
- @mui/x-tree-view
- @uiw/codemirror-extensions-mentions
- @uiw/codemirror-theme-dracula
- canvas-confetti
- compute-cosine-similarity
- dayjs
- eslint-linter-browserify
- file-saver
- jszip
- ndjson-parse
- @nasco/nexus-data-model

### Unused Dependencies Pre-rework
- @eslint/js
- @stylistic/eslint-plugin
- eslint
- eslint-plugin-react
- eslint-plugin-react-hooks
- eslint-plugin-react-refresh
- globals
- sass
- typescript
- typescript-eslint

### Unused Dependencies After-rework
None

### Unused DevDependencies After-rework
- typescript
- typescript-eslint

### Missing Dependencies
- @codemirror/commands
- @codemirror/view
- @react-pdf-viewer/full-screen
- @react-pdf-viewer/toolbar
- @dnd-kit/utilities

## packages/common

### Unused Dependencies Pre-rework
None

### Unused Dependencies Pre-rework
- console-table-printer
- typescript

### Unused Dependencies After-rework
None

### Unused DevDependencies After-rework
- typescript

### Missing Dependencies
- @nasco/nexus-constants
- @nasco/nexus-data-model
- @aws-sdk/client-s3
- @aws-sdk/s3-request-presigner
- @aws-sdk/client-lambda
- @aws-sdk/client-dynamodb
- @aws-sdk/util-dynamodb
- @aws-sdk/client-redshift-data
- @aws-sdk/client-cognito-identity-provider

## packages/constants

### Unused Dependencies Pre-rework
- @nasco/nexus-common

### Unused Dependencies Pre-rework
- typescript

### Unused Dependencies After-rework
None

### Unused DevDependencies After-rework
- typescript

### Missing Dependencies
None

## packages/core

### Unused Dependencies Pre-rework
None

### Unused Dependencies Pre-rework
- typescript

### Unused Dependencies After-rework
None

### Unused DevDependencies After-rework
- typescript

### Missing Dependencies
None

## packages/data_model

### Unused Dependencies Pre-rework
- @nasco/nexus-core

### Unused Dependencies Pre-rework
- typescript

### Unused Dependencies After-rework
None

### Unused DevDependencies After-rework
- typescript

### Missing Dependencies
None

## packages/definitions

### Unused Dependencies Pre-rework
- @nasco/nexus-sdk

### Unused Dependencies Pre-rework
- typescript

### Unused Dependencies After-rework
None

### Unused DevDependencies After-rework
- typescript

### Missing Dependencies
- @aws-sdk/client-dynamodb

## packages/sdk

### Unused Dependencies Pre-rework
None

### Unused Dependencies Pre-rework
- typescript

### Missing Dependencies
- @nasco/nexus-tester
- vitest

### Unused Dependencies After-rework
None

### Unused DevDependencies After-rework
- typescript

## Notes
- "Unused Dependencies" are listed in `dependencies` but not used in code.
- "Unused DevDependencies" are in `devDependencies` but not used.
- "Missing Dependencies" are used in code but not listed in package.json.
- Some missing dependencies might be peer dependencies or false positives; review carefully.
- Consider removing unused dependencies to reduce bundle size and maintenance overhead.
- For missing dependencies, add them to the appropriate section in package.json.</content>
<parameter name="filePath">unused-dependencies-report.md

## Command used to make confront of the changes
cd /c/Projects/nexus && for dir in . apps/dev_ops apps/nexus_backend apps/nexus_frontend packages/common packages/constants packages/core packages/data_model packages/definitions packages/sdk; do echo "=== $dir ==="; (cd "$dir" && npx depcheck); done