# Working with the Google Cloud Console and Cloud Shell

# **Overview**

In this lab, you become familiar with the Google Cloud web-based interface. There are two integrated environments: a GUI (graphical user interface) environment called the Google Cloud console, and a CLI (command-line interface) called Cloud Shell. In this lab, you use both environments.

Here are a few things you need to know about the Cloud console:

- The Cloud console is under continuous development, so occasionally the graphical layout changes. This is most often to accommodate new Google Cloud features or changes in the technology, resulting in a slightly different workflow.
- You can perform most common Google Cloud actions in the Cloud console, but not all actions. In particular, very new technologies or sometimes detailed API or command options are not implemented (or not yet implemented) in the Cloud console. In these cases, the command line or the API is the best alternative.
- The Cloud console is extremely fast for some activities. The Cloud console can perform multiple actions on your behalf that might require many CLI commands. It can also perform repetitive actions. In a few clicks you can accomplish activities that would require a lot of typing and would be susceptible to typing errors.
- The Cloud console is able to reduce errors by offering only valid options through its menus. It can leverage access to the platform "behind the scenes" through the SDK to validate configuration before submitting changes. A command line can't do this kind of dynamic validation.

# **Objectives**

In this lab, you learn how to perform the following tasks:

- Get access to Google Cloud.
- Use the Cloud console to create a Cloud Storage bucket.
- Use Cloud Shell to create a Cloud Storage bucket.
- Become familiar with Cloud Shell features.