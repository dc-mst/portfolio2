---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Copilot Chat first impressions"
url: "/copilot-chat-first-impressions"
subtitle: "Some preliminary testing on the Copilot chat extension"
summary: "I finally got my invite in the closed beta"
authors: [ d-cmst ]
tags: [ GitHub, Copilot, AI, chatbot]
categories: [ Code editors, chatbot, AI ]
keywords: [VS Code, Copilot, AI]
date: 2023-05-19
publishDate: 2023-05-19
lastmod: 2023-05-19
featured: true
draft: false


# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

I finally got an invitation for the Copilot chat extension closed beta, available in Visual Studio Code and Visual Studio 2022. The extension presents numerous opportunities for developers aiming to enhance their productivity and efficiency. By offering context-based suggestions and addressing coding inquiries, GitHub Copilot chat effectively assists developers in saving time and minimizing errors in their code.


> Greetings, @d-cmst! I am your Copilot, ready to expedite your tasks and provide guidance. I possess the ability to identify issues, clarify code, and even enhance it (source: @d-cmst). Here are some installation, setup, and usage tips that summarize various capabilities to empower developers with smarter and faster workflows. Please note that these tips are specific to the VS Code offering and do not encompass the Visual Studio IDE counterpart.

## Acquiring the Necessary Components

To access GitHub Copilot Chat, the following prerequisites must be fulfilled:

- Active GitHub subscription: Ensure that the GitHub ID you intend to use has an active subscription to GitHub Copilot and matches the ID you provided while joining the GitHub Copilot chat waitlist.
- Visual Studio Code - Insiders build: The Insiders program grants early access to new features and updates. This allows developers to test novel functionalities and provide feedback to the development team before the updates are released to the general public.
- GitHub Copilot Nightly Extension: This extension offers early access to upcoming features and updates before their official release. It undergoes more frequent updates compared to the regular GitHub Copilot extension and may contain experimental features not yet available in the stable release. The extension has been installed over 388,000 times.

Once the Insiders editor is launched, you can install the Nightly extension by navigating to the Extensions tab through the conventional methods (e.g., clicking the icon in the activity panel or using Cmd+Shift+X on Mac or Ctrl+Shift+X on Windows), searching for the extension, and then installing it. You may need to sign in to GitHub and authorize the Insiders build if you haven't already done so. Following the installation, the chat interface will be accessible through a new Chat icon in the activity panel, although restarting the editor may be required for it to appear.

## Exploring the Functionalities

Now, let's delve into what you can accomplish with this new chat integration:

To set a positive tone for the day, you can greet your new assistant with a "Good morning!" This prompts a cheerful response of "Good morning! How can I assist you with your programming needs today?" accompanied by a suggestion for potential questions to continue the conversation.

For a historical perspective on the development of chat integration and its functionalities, Microsoft's introductory blog post on March 30 is an excellent starting point.

While the blog post outlines various capabilities and benefits, it also emphasizes that 

> having a two-way conversation helps you decide what is right and what is wrong. Large language models are not perfect, and they don't 'think.' They simply figure out the next best word to respond with (granted, they are pretty good at this).

and

> As the Pilot, you are always in charge, and you decide which of Copilot's suggestions to take and what code to bring into your workspace. The ability to ask clarifying questions or provide additional specifics helps you make those key decisions.

In terms of functionalities, the tool provides an initial overview:

> I'm here to help you get things done faster. I can identify issues, explain and even improve code.

While you can ask general questions, the tool excels in assisting with your code. For example, you can:

- Generate unit tests for your code.
- Request an explanation of selected code.
- Obtain proposed fixes for bugs in your code.

Additionally, the tool offers support in the following areas:

### Interactive Programming

The chat feature enables developers to interact with GitHub Copilot in a conversational manner. You can request it to write code, explain code snippets, and even learn from it. This fosters a more engaging and interactive coding experience.

### Code Explanation

A standout feature of the chat functionality is the ability to ask GitHub Copilot to explain specific portions of your code. This proves beneficial, particularly for beginners or when working with a new programming language or framework, as it serves as a valuable learning tool.

### Code Generation
You can rely on GitHub Copilot to generate specific code segments. For instance, you can request it to create a function that performs a particular task, and it will generate the code accordingly.

### Code Review
GitHub Copilot excels in reviewing your code and providing suggestions for improvements. This aids in identifying potential issues before they become problems and enhances the overall quality of your code.

### Learning Tool
The chat feature serves as an effective learning tool. You can pose questions to GitHub Copilot about the usage of specific functions or methods, and it will furnish explanations and examples accordingly.

Several of these functionalities can be accessed through slash commands tailored for common tasks. By typing "/", developers can select from various available commands, such as:

- /vscode - Questions related to VS Code.
- /tests - Generation of unit tests for the selected code.
- /simplify - Simplification of the selected code.
- /fix - Proposing fixes for problems in the selected code.
- /explain - Step-by-step explanation of how the selected code functions.
- /ext - Queries about VS Code extension development.
- /help - General assistance concerning GitHub Copilot.

Regarding the first item, inquiring about VS Code, some possible questions include:

- How do I create a new file in Visual Studio Code?
- What is the keyboard shortcut for opening the Command Palette in Visual Studio Code?
- How do I install an extension in Visual Studio Code?
- What is the difference between a workspace and a folder in Visual Studio Code?
- How do I debug my code in Visual Studio Code?
- How do I change the theme in Visual Studio Code?
- How do I customize my keyboard shortcuts in Visual Studio Code?
- How do I split my editor window in Visual Studio Code?
- How do I search for a specific file in my project in Visual Studio Code?
- How do I use Git with Visual Studio Code?

Regarding the "/help" command, valuable advice is provided, such as:

> Start by asking questions as if you were talking to a real programmer. This means including implementation details, asking clarifying questions, and providing feedback like logs or error messages.

Moreover, several tips are offered to ensure a productive conversation:

Display the code you wish to discuss by having the relevant files open, preferably with the most important lines selected.
Refine the conversation by asking follow-up questions, providing clarifications, sharing errors, and so on.
Review the suggested code and offer feedback on issues or improvements, enabling iterative enhancements.
It is worth noting that the chat integration is unable to insert HTML list item tags, `<li>` and `</li>`, around a list of sentences, as demonstrated in this article. Despite numerous attempts, the chat function failed to achieve this task, resulting in blank space.

In contrast, when I asked ChatGPT (Plus version, incorporating GPT-4 and the WebPilot plugin) about writing the prompt, it also encountered difficulties. However, ChatGPT performed admirably by suggesting an alternative prompt. This indicates that the chat integration mentioned earlier, "Copilot meets ChatGPT," may not accurately describe the full capabilities of GitHub Copilot chat, as ChatGPT can accomplish tasks that the chat integration cannot.

While it is possible that GitHub Copilot chat possesses functionalities beyond those of ChatGPT (except for HTML list item tags), the best way to ascertain this is by gaining access to the tool and exploring its capabilities firsthand.

While this article primarily focuses on the VS Code-specific aspects, many of the details also apply to the integration of GitHub Copilot chat into the Visual Studio IDE. To explore further information in that regard, Microsoft's blog post from March 22 titled "GitHub Copilot chat for Visual Studio 2022" serves as an excellent starting point.