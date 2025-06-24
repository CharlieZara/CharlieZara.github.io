# Setting up the HarmonyOS Application Development Environment
As a smart operating system for multiple devices across various scenarios, **HarmonyOS** is gradually making its mark in the market. To enter the **HarmonyOS** ecosystem, developers need to set up an efficient development environment. This article will provide a detailed introduction on how to set up the **HarmonyOS** development environment, especially on how to install and configure **DevEco Studio**.
## Precondition
Before starting to set up the development environment, please make sure that your computer meets the following requirements:

>  - **operating system:**
Windows 10/11 64-bit
macOS (X86) versions 10.15 and above, macOS (ARM) versions 11 and above
>  - **internal storage:**
> At least 8GB, recommended 16GB
>  - **hard disk:**
> At least 100GB of available space
>  - **resolution ratio:**
> 1280 x 800 pixels and above
## 1.Download and install DevEco Studio
DevEco Studio is built based on the open-source version of IntelliJ IDEA Community, providing a one-stop development platform for applications and services on the HarmonyOS and OpenHarmony systems.
### 1.1.下载DevEco Studio
- Visit the official website of Huawei Developer Alliance: https://developer.harmonyos.com
![huawei site](https://i-blog.csdnimg.cn/direct/e5765bf4fa024eed86981d934b9bf5f6.png)

- Enter the "Development" section and select "Download DevEco Studio"

![huawei site](https://i-blog.csdnimg.cn/direct/03a7c900561c4e8abaa7a1b35fe0c3a0.png)
- Here, select the corresponding version according to your own operating system (the blogger's operating system here is Windows 11 64-bit)

![DevEco Studio](https://i-blog.csdnimg.cn/direct/24cf7df88b054bdfac4ea32fc5a2bd0e.png)
### 1.2.安装DevEco Studio
> - **Windows system:**
> Extract the devecostudio-windows-5.0.5.200.zip file.
Double-click the downloaded installation package to run it (or right-click and run as an administrator).
Select the installation path (it is recommended to install it on a non-system drive).
Check the components you want to install, and click "Install" until the process is completed.
> - **MacOS system:**
> Double-click on the downloaded "deveco-studio-xxxx.dmg" software package.
On the installation interface, drag "DevEco-Studio.app" to "Applications", and wait for the installation to complete.

Here, the blogger takes the 64-bit Windows 11 operating system as an example:

![install](https://i-blog.csdnimg.cn/direct/f28cce20920949a2aa92a7c2eba952dd.png)

![install](https://i-blog.csdnimg.cn/direct/6b2c01dc04fe42ebb3fe80291367001a.png)
> Here, you can choose the installation directory yourself (the blogger's installation is on the D drive)

![install](https://i-blog.csdnimg.cn/direct/7ad77cfba04846b884e04c38d1c2c6f6.png)
> If you check the option for the more detailed PATH variable here, you won't have to configure the environment variables yourself (a boon for the lazy ones)!

![install](https://i-blog.csdnimg.cn/direct/2305543cc1f44554a69a16bf06c241b0.png)

> After clicking "Install", you can simply wait for the good news.

![install](https://i-blog.csdnimg.cn/direct/51398bf80b934f68a4c5b421012caca8.png)

![install](https://i-blog.csdnimg.cn/direct/dc604963a624408ea86b722368b241b9.png)

> OK, let's save the file first. We'll wait until the blogger restarts Windows.

## 2. Configure the development environment

### 2.1. Run DevEco Studio
![install](https://i-blog.csdnimg.cn/direct/572b37ea5ba0436ebb089e51b2a86010.png)


> When running for the first time, we select "Do not import settings" and click "OK"

![install](https://i-blog.csdnimg.cn/direct/ae72e69937bf4f399f2ff5cfb87faad3.png)

> OK. Here, the "anti-addiction" terms are accepted. Once you accept them, you can start using DevEco Studio to develop your first HarmonyOS application.

## 3. Create the first project
After the installation is completed, you can start creating the first HarmonyOS project:

### 3.1. Start DevEco Studio
- If it is the first time to start DevEco Studio, click "Created Project" to create a project.
- If you have already entered the development interface of DevEco Studio, select "File" > "New" > "New Project" in the upper right corner.

![install](https://i-blog.csdnimg.cn/direct/b18f87aca24f4b229bd671b35df056ce.png)

![install](https://i-blog.csdnimg.cn/direct/bbb702fec78c474cbe8d773be55f3f81.png)
### 3.2. Selecting Templates
Select "Application" for application development, select "Empty Ability", and click "Next" to proceed with the next configuration. If you need to develop Native-related projects, please choose the "Native C++" template. For more details and introductions about the templates, please refer to [Huawei Harmony OS Development Guide > Introduction to Engineering Templates](https://developer.huawei.com/consumer/cn/doc/harmonyos-guides-V13/ide-template-V13)

### 3.3. Configuration Project
![install](https://i-blog.csdnimg.cn/direct/5d8858cef46147b1bc6b71526a155973.png)

> - For the compatible SDK, select "5.0.1(13)". Keep the other parameters as default.
> 【Note】: The bundle name is composed of three parts separated by ".".

Click "Finish", and the tool will automatically generate sample code and related resources. Wait for the project to be created.

### 3.4. Project Structure [ArkTS Project Directory Structure (Stage Model)]

![content](https://i-blog.csdnimg.cn/direct/78a94c98d7ac488cb4c512df3bc24c53.png)

> - **AppScope > app.json5:** Global configuration information for the application. Refer to the app.json5 configuration file for details.
> - **entry:** HarmonyOS engineering module. Compilation and build generate an HAP package.
> > - **src > main > ets:** Used to store the ArkTS source code.
> > - **src > main > ets > entryability:** The entry point of the application/service.
> > -**src > main > ets > entrybackupability:** The application provides extended backup and recovery capabilities.
> > - **src > main > ets > pages:** The pages included in the application/service.
> > - s**rc > main > resources:** Used to store resource files used by the application/service, such as graphics, multimedia, strings, layout files, etc. Regarding resource files, refer to the resource classification and access.
> > - **src > main > module.json5:** Module configuration file. Mainly contains configuration information for the HAP package, configuration information for the application/service on specific devices, and global configuration information for the application/service. Specific configuration file explanations can be found in the module.json5 configuration file.
> > - **build-profile.json5:** Current module information, compilation information configuration items, including buildOption, targets configuration, etc.
> > - **hvigorfile.ts:** Module-level compilation and build task script.
> > - **obfuscation-rules.txt:** Obfuscation rules file. When code obfuscation is enabled and compiled in Release mode, the code will be compiled, obfuscated, and compressed to protect the code assets. See enabling code obfuscation.
 > - **oh-package.json5:** Used to describe package name, version, entry file (type declaration file), and dependencies, etc.
> - **oh_modules:** Used to store third-party library dependency information. 
> - **oh-package.json5:** Primarily used to describe global configurations, such as: dependency overrides, dependency relationship overrides (overrideDependencyMap), and parameterized configurations (parameterFile), etc.

## 4. Debugging and running the project
In the side toolbar at the top right corner of the editing window, click "Previewer" to open the previewer.

![settings](https://i-blog.csdnimg.cn/direct/925e165d9b0e4840b86ea9ae33c6abfe.png)

Then click the green play button to run the project:
![settings](https://i-blog.csdnimg.cn/direct/c041052e66d8477f96d5426a0c59aa30.png)

The blogger has chosen a phone device (as shown in the figure below for the operation effect):
![settings](https://i-blog.csdnimg.cn/direct/0fb4d07014244610895757e00adab688.png)

![view](https://i-blog.csdnimg.cn/direct/74a7435f18e1467fa5328a10e009f6c6.png)
> This article was originally published on CSDN. The original author and the current author are the same person. Welcome everyone to discuss together.

