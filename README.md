# Instruction

Quick start instructions for Vue.js + Electron

![Screenshot](https://github.com/afonichev/vue-electron/blob/master/vue-electron.png "Vue + Electron = ❤️")

#### Getting Started
```bash
# Install Vue, if not yet installed
# yarn global add @vue/cli
npm i -g @vue/cli

# Create Vue project
vue create vue-project-name

# Go to root project folder
cd vue-project-name

# Install Vue plugin
vue add electron-builder

# Start app
# yarn electron:serve
npm run electron:serve

# Build app
# yarn electron:build
npm run electron:build
```

#### Build Configurations
Create file **vue.config.js** in root **vue-project-name**

```javascript
module.exports = {
    pluginOptions: {
        electronBuilder: {
            builderOptions: {
                asarUnpack: [
                    "node_modules"
                ],
                win: {
                    target: "zip",
                    icon: "./public/favicon.ico" // Required favicon size 256x256
                }
            }
        }
    }
}
```
All options you can see on the [official website](https://www.electron.build/configuration/configuration) of electron-builder
