<div align="center">

![project hero](https://i.hizliresim.com/q5vyn9r.png)

# Deer Imagine

#### To learn more about Invoke, or implement our Business solutions, visit [aideer.tech]

[![discord badge]][discord link] [![latest release badge]][latest release link] [![github stars badge]][github stars link] [![github forks badge]][github forks link] [![CI checks on main badge]][CI checks on main link] [![latest commit to main badge]][latest commit to main link] [![github open issues badge]][github open issues link] [![github open prs badge]][github open prs link] [![translation status badge]][translation status link]

</div>

Deer is a leading creative engine built to empower professionals and enthusiasts alike. Generate and create stunning visual media using the latest AI-driven technologies. Deer offers an industry leading web-based UI, and serves as the foundation for multiple commercial products.

Deer is available in two editions:

| **Community Edition**                                                                                                      | **Professional Edition**                                                                            |
|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| **For users looking for a locally installed, self-hosted and self-managed service**                                         | **For users or teams looking for a cloud-hosted, fully managed service**                            |
| - Free to use under a commercially-friendly license                                                                         | - Monthly subscription fee with three different plan levels                                         |
| - Download and install on compatible hardware                                                                               | - Offers additional benefits, including multi-user support, improved model training, and more                          |
| - Includes all core studio features: generate, refine, iterate on images, and build workflows                               | - Hosted in the cloud for easy, secure model access and scalability                                               |
| Quick Start -> [Installation and Updates][installation docs]                                                                     | More Information -> [www.invoke.com/pricing](https://www.invoke.com/pricing)                        |


![Highlighted Features - Canvas and Workflows](https://github.com/invoke-ai/InvokeAI/assets/31807370/708f7a82-084f-4860-bfbe-e2588c53548d)

# Documentation
| **Quick Links**                                                                                                      | 
|----------------------------------------------------------------------------------------------------------------------------|
|  [Installation and Updates][installation docs] - [Documentation and Tutorials][docs home] - [Bug Reports][github issues] - [Contributing][contributing docs]  | 

</div>

## Quick Start

1. Download and unzip the installer from the bottom of the [latest release][latest release link].
2. Run the installer script.

   - **Windows**: Double-click on the `install.bat` script.
   - **macOS**: Open a Terminal window, drag the file `install.sh` from Finder into the Terminal, and press enter.
   - **Linux**: Run `install.sh`.

3. When prompted, enter a location for the install and select your GPU type.
4. Once the install finishes, find the directory you selected during install. The default location is `C:\Users\Username\invokeai` for Windows or `~/invokeai` for Linux/macOS.
5. Run the launcher script (`invoke.bat` for Windows, `invoke.sh` for macOS and Linux) the same way you ran the installer script in step 2.
6. Select option 1 to start the application. Once it starts up, open your browser and go to <http://localhost:9090>.
7. Open the model manager tab to install a starter model and then you'll be ready to generate.

More detail, including hardware requirements and manual install instructions, are available in the [installation documentation][installation docs].

## Docker Container

We publish official container images in Github Container Registry: https://github.com/invoke-ai/InvokeAI/pkgs/container/invokeai. Both CUDA and ROCm images are available. Check the above link for relevant tags.

> [!IMPORTANT]
> Ensure that Docker is set up to use the GPU. Refer to [NVIDIA][nvidia docker docs] or [AMD][amd docker docs] documentation.

### Generate!

Run the container, modifying the command as necessary:

```bash
docker run --runtime=nvidia --gpus=all --publish 9090:9090 ghcr.io/invoke-ai/invokeai
```

Then open `http://localhost:9090` and install some models using the Model Manager tab to begin generating.

For ROCm, add `--device /dev/kfd --device /dev/dri` to the `docker run` command.

### Persist your data

You will likely want to persist your workspace outside of the container. Use the `--volume /home/myuser/invokeai:/invokeai` flag to mount some local directory (using its **absolute** path) to the `/invokeai` path inside the container. Your generated images and models will reside there. You can use this directory with other InvokeAI installations, or switch between runtime directories as needed.

### DIY

Build your own image and customize the environment to match your needs using our `docker-compose` stack. See [README.md](./docker/README.md) in the [docker](./docker) directory.

## Troubleshooting, FAQ and Support

Please review our [FAQ][faq] for solutions to common installation problems and other issues.

For more help, please join our [Discord][discord link].

## Features

Full details on features can be found in [our documentation][features docs].

### Web Server & UI

Invoke runs a locally hosted web server & React UI with an industry-leading user experience.

### Unified Canvas

The Unified Canvas is a fully integrated canvas implementation with support for all core generation capabilities, in/out-painting, brush tools, and more. This creative tool unlocks the capability for artists to create with AI as a creative collaborator, and can be used to augment AI-generated imagery, sketches, photography, renders, and more.

### Workflows & Nodes

Invoke offers a fully featured workflow management solution, enabling users to combine the power of node-based workflows with the easy of a UI. This allows for customizable generation pipelines to be developed and shared by users looking to create specific workflows to support their production use-cases.

### Board & Gallery Management

Invoke features an organized gallery system for easily storing, accessing, and remixing your content in the Invoke workspace. Images can be dragged/dropped onto any Image-base UI element in the application, and rich metadata within the Image allows for easy recall of key prompts or settings used in your workflow.

### Other features

- Support for both ckpt and diffusers models
- SD1.5, SD2.0, SDXL, and FLUX support
- Upscaling Tools
- Embedding Manager & Support
- Model Manager & Support
- Workflow creation & management
- Node-Based Architecture

## Contributing

Anyone who wishes to contribute to this project - whether documentation, features, bug fixes, code cleanup, testing, or code reviews - is very much encouraged to do so.

Get started with contributing by reading our [contribution documentation][contributing docs], joining the [#dev-chat] or the GitHub discussion board.

We hope you enjoy using Invoke as much as we enjoy creating it, and we hope you will elect to become part of our community.
