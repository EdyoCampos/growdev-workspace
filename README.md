# growdev-scrapbook-api

yarn init -y
yarn add typescript -D
yarn add express cors
yarn add @types/node @types/typescript @types/express @types/cors ts-node-dev -D

yarn tsc --init

alterar tsconfig.json:
{
  "compilerOptions": {
    "target": "es2020",
    "module": "commonjs",
    "rootDir": "./src",
    "outDir": "./dist",
    "esModuleInterop": true,
    "forceConsistentCasingInFileNames": true,
    "strict": true,
    "skipLibCheck": true
  }
}

criar pasta src

alterar package.json, e colocar scripts:
"scripts": {
    "dev": "ts-node-dev --respawn --transpile-only ./src/index.ts",
    "build": "tsc",
    "start": "node ./dist"
}
