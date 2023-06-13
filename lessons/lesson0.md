---
layout: default
title: Lesson 0 - Using your IDE
nav_order: 0
parent: Lessons
---
<!-- 
This page is an example lesson template.
Add, edit, or remove any content below for the workshop in question. -->

<!-- Putting a {: .no_toc} above a header removes it from the table of contents -->

{: .no_toc}  
# Lesson 0 - Using your IDE

This lesson will go over the basic functionality of the IDEs highlighted in the Preparation page.

<!-- This is your table of contents. You don't need to touch it, it automatically creates it when you add or remove headers. If you do not want a header to be included, put {: .no_toc } above the header line, as you can see above with Lesson 1 - Lesson Name. Make sure that there's also an empty line above {: .no_toc }... Markdown is picky about this :( -->
<details markdown="block">
  <summary>
    Table of Contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

<!-- Here are your learning objectives. Just like in the introduction, but more specific for this lesson. -->
## Lesson Objectives
- Learn how to create, edit, and run Python files.

<!-- A video for your lesson (if applicable) -->
<!-- ## Lesson Video
The following video demonstrates each of the steps outlined below in text.

<iframe height="416" width="100%" allowfullscreen frameborder=0 src="https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false"></iframe>
[View original here.](https://echo360.ca/media/a65689c0-c35c-4f33-9c12-f0ac97883f54/public?autoplay=false&automute=false) -->

<!-- Text content format for your lessons if you don't want to rely on videos, or want to provide another format of learning consumption. -->

## Choose your IDE

Follow the instructions outlined in one of the dropdown menus below.

<details markdown="1">
<summary> Jupyter Notebook - Recommended </summary>

If you haven't already, [sign in to Jupyter Notebook](https://mcmaster.syzygy.ca/).

The home page of Jupyter Notebook is the file explorer, where you can access any files you created. If it's your first time using Jupyter Notebook, it'll be empty. To create a new Python Notebook file (.ipynb), click on the `New` button at the top right and select `Python3 (ipykernel)`.

<img width="100%" src="../assets/img/lessons/jupyter1.png" style="border: 2px solid #000;">

<br>

You should automatically be sent to your Python Notebook environment. It should look like the screenshot below.
- If you ever want to go back to the home page, click on the JupyterHub logo at the top left.
- You can rename your Python Notebook file by clicking on the "Untitled" text beside the JupyterHub logo.
- To save your file, use the `Save and Checkpoint` button with a disk icon found below the JupyterHub logo. You can also use `Ctrl` + `S` shortcut (or `Cmd` + `S` for Mac users) to save.

<img width="100%" src="../assets/img/lessons/jupyter2.png" style="border: 2px solid #000;">

<br>

Your Python Notebook file consists of code blocks. You can write Python code in these blocks and run them using the `Run` button. If there's any output, it will be shown directly below that code block.

{: .warning}
If a code block is taking too long to run, you might have encountered an infinite loop. Use the `interrupt the kernel` button beside the `Run` button to stop it.

<img width="100%" src="../assets/img/lessons/jupyter3.png" style="border: 2px solid #000;">

<br>

To create new code blocks, click on the `+` button beside the `Save and Checkpoint` button.

<img width="100%" src="../assets/img/lessons/jupyter4.png" style="border: 2px solid #000;">

{: .note }
No matter what code block you're on, Python Notebook will keep the data of all previously run code blocks. If you're opening up a Notebook, or your Notebook connection resets, you have to run every block code from the start.

</details>

<details markdown="1">
<summary> Google Colab - Online Alternative</summary>

If you haven't already, [sign in to Google Colab](https://colab.research.google.com/).

After signing in, you may encounter the `Recent` page below. This is where you'll be able to open up recent Python Notebook files (.ipynb). To create a new Python Notebook file, we'll need to `Cancel` out of this pop-up.

<img width="90%" src="../assets/img/lessons/colab1.png" style="border: 2px solid #000;">

<br>

Navigate to the top left of your screen, click on `File`, and then click on `New notebook`.

<img width="70%" src="../assets/img/lessons/colab2.png" style="border: 2px solid #000;">

<br>

You should automatically be sent to your Python Notebook environment. It should look like the screenshot below.
- To view all of your Colab files, click on the Colab logo at the top left. 
- You can rename your Python Notebook file by clicking on the "Untitled.ipynb" text beside the Colab logo.
- Google Colab automatically saves your work, no need for manual saving.

<img width="100%" src="../assets/img/lessons/colab3.png" style="border: 2px solid #000;">

<br>

Your Python Notebook file consists of code blocks. You can write Python code in these blocks and run them using the `Run` button. If there's any output, it will be shown directly below that code block.

{: .warning}
If a code block is taking too long to run, you might have encountered an infinite loop. Use the `interrupt the kernel` button beside the `Run` button to stop it.

<img width="100%" src="../assets/img/lessons/colab4.png" style="border: 2px solid #000;">

<br>

To create new code blocks, click on the `+` button beside the `Save and Checkpoint` button.

{: .note }
No matter what code block you're on, Python Notebook will keep the data of all previously run code blocks. If you're opening up a Notebook, or your Notebook connection resets, you have to run every block code from the start.

<img width="100%" src="../assets/img/lessons/colab5.png" style="border: 2px solid #000;">

</details>

<details markdown="1">
<summary> Anaconda - Local Version of Jupyter Notebooks </summary>

If you haven't already downloaded and installed Anaconda:
- Download and install at <https://www.anaconda.com/>.
- Follow along with the guide for your OS system for installation instructions.
  - Windows: <https://docs.anaconda.com/free/anaconda/install/windows/>
  - MacOS: <https://docs.anaconda.com/free/anaconda/install/mac-os/>
  - Linux: <https://docs.anaconda.com/free/anaconda/install/linux/>

Once that's installed, open up the **Anaconda Navigator** application. Included in the Anaconda package are four great tools/IDEs to create Python files with. JupyterLab, Jupyter Notebooks, Spyder, and Visual Studio Code. 

Spyder and Visual Studio Code are standalone IDEs, whereas JupyterLab and Jupyter Notebooks opens up locally in your browser. For the purposes of this workshop, we recommend you use Jupyter Notebooks.

<img width="100%" src="../assets/img/lessons/anaconda1.png" style="border: 2px solid #000;">

<br>

When you first launch Jupyter Notebooks, you will see a file explorer. Go to the location you want to store your Python files in, (I recommend making a new "Python" folder in the Documents directory).

<img width="100%" src="../assets/img/lessons/anaconda2.png" style="border: 2px solid #000;">

<br>

To create a new Python Notebook file (.ipynb), click on the `New` button at the top right and select `Python3 (ipykernel)`.

<img width="100%" src="../assets/img/lessons/anaconda3.png" style="border: 2px solid #000;">

<br>

You should automatically be sent to your Python Notebook environment. It should look like the screenshot below.
- If you ever want to go back to the home page, click on the JupyterHub logo at the top left.
- You can rename your Python Notebook file by clicking on the "Untitled" text beside the JupyterHub logo.
- To save your file, use the `Save and Checkpoint` button with a disk icon found below the JupyterHub logo. You can also use `Ctrl` + `S` shortcut (or `Cmd` + `S` for Mac users) to save.

<img width="100%" src="../assets/img/lessons/anaconda4.png" style="border: 2px solid #000;">

<br>

Your Python Notebook file consists of code blocks. You can write Python code in these blocks and run them using the `Run` button. If there's any output, it will be shown directly below that code block.

{: .warning}
If a code block is taking too long to run, you might have encountered an infinite loop. Use the `interrupt the kernel` button beside the `Run` button to stop it.

<img width="100%" src="../assets/img/lessons/anaconda5.png" style="border: 2px solid #000;">

<br>

To create new code blocks, click on the `+` button beside the `Save and Checkpoint` button.

<img width="100%" src="../assets/img/lessons/anaconda6.png" style="border: 2px solid #000;">

{: .note }
No matter what code block you're on, Python Notebook will keep the data of all previously run code blocks. If you're opening up a Notebook, or your Notebook connection resets, you have to run every block code from the start.

</details>

<!-- Summarize your learning objectives here. It acts as a reminder to the learner about what they just learned, as well as a checklist for you to make sure you covered everything you wished to cover. -->
## Key Points / Summary
- There are many ways to create, edit, and run Python files.

