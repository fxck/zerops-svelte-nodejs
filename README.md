# Zerops + Svelte - Nodejs

![Header Image](/header.png)

A Nodejs Svelte example for Zerops which you can deploy in 2 simple steps.

**Features**

- Svelte
- Tailwind
- Prettier

## Instructions to Deploy on Zerops

1. [Create an account](https://app.zerops.io/registration) and locate the "Import project" button in the top left menu.

2. Paste the Project Yaml

```yaml
project:
  name: zerops-svelte
services:
  - hostname: sveltenode
    type: nodejs@20
    buildFromGit: https://github.com/fxck/zerops-svelte-nodejs
    ports:
      - port: 3000
        httpSupport: true
    enableSubdomainAccess: true
    minContainers: 1
```

If you still find yourself stuck in the process join our [Discord community](https://discord.gg/5ptAqtpyvh).
