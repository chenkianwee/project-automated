---
title: "Development of Project Specific Single Task Applications"
date: 2025-8-10T00:00:00-04:00
weight: 1
---
The use of Python Beeware and Pyscript to develop applications for sharing your Python scripts to non-programmers.  

10 mins read\
Written by Kian Wee Chen\
Published on Aug 11th 2025

# Sharing Your Python Scripts is Difficult
Have you ever had this similar experience? I wrote a Python script to streamline a task in the project. It is quick and dirty and pieced together from various third-party Python libraries. The script might not work outside of this project context, but it worked for this particular task for this project for now. It will ease the project workload if this script was available to the team. However, the script kind of only works on my computer and it is a stretch to ask my colleagues who have not wrote codes before to setup their computer to execute the script. In the end, the script was used only by me, some times, and everyone else either avoid the task or still did it manually. I have documented an experience of similar nature <a href="https://www.itcon.org/paper/2022/49" target="_blank">working with a sculpture artist in a paper here</a>. If only there was a quick way to package the script into a simple Graphic User Interface (GUI) for internal deployment. I recently gave  <a href="https://beeware.org/" target="_blank">Beeware</a> and <a href="https://pyscript.net/" target="_blank">Pyscript</a> a go and I think they are sufficiently matured to resolve the issue I had described above.

# Python is a Powerful Language for Streamlining and Automating Tasks but ...
You can probably find a similar example or a useful third-party library in Python for most of the tasks you are thinking of streamlining or automating in the Architecture, Engineering, Construction and Operation (AECO) context. This makes Python a very useful tool to have in a project. However, the problem with Python has been in distribution and deployment of your programs. The Python community is aware of that and in response the Beeware and Pyscript projects are borned. Beeware is a framework that consists of a suite of tools, two main libraries are <a href="https://toga.readthedocs.io/en/stable/" target="_blank">Toga</a> for GUI and <a href="https://beeware.org/project/briefcase/" target="_blank">Briefcase</a> for packaging. By using the Beeware framework, you can deploy your application on all the supported platforms like Linux, MacOS and Windows. 

In the meantime, they only have partial support for Android, iOS and web applications, but it seems like the support will probably increase considering the popularity of mobile devices and cloud-based services. This means that you can also deploy your Python scripts as mobile applications and frontend web applications. The underlying web application deployment uses Pyscript, which allows you to execute Python codes in the browser. The power of Pyscript is that it allows you to install most of the powerful third-party libraries like Numpy and Pandas from PyPI using pip install. Making deploying your Python frontend web applications that depends on third-party libraries fairly straightforward. Frontend web applications are very convenient in comparison to local program as no installation is required, just visit the website and everything will be downloaded, installed and ran locally in your web browser. 

Beeware and Pyscript sounded good on paper. I finally got the chance to test it and see how well both of these tools works.

# A Simple PDF tool: PdfAutomated
I wrote a PDF tool called PdfAutomated for myself. I want a tool that can merge and extract pages and reduce the size of PDFs as I always have to do this. I was using <a href="https://pdfsam.org/" target="_blank">PDFSam</a> to do the merging and extraction. Size compression is a paid feature and not available on the basic version. I used online tools to do the compression, which I am not fond of sending my PDF to servers of dubious free online tools that I found with a single search. I decided to build a tool to streamline my PDF-related works. As expected there is already a fairly matured Python library, pypdf, for reading and writing PDFs. I spend a weekend learning Beeware, wrote the codes and packaged it for Ubuntu and Windows (I do not have access to a MacOS machine). You can <a href="https://github.com/chenkianwee/pdfautomated/releases" target="_blank">download the binaries here</a>. The three images below shows the GUI.

![image-title-here](/images/blogs/app/pdfautomated_merge.png){:class="img-responsive"}
![image-title-here](/images/blogs/app/pdfautomated_extract.png){:class="img-responsive"}
![image-title-here](/images/blogs/app/pdfautomated_reduce.png){:class="img-responsive"}

Beeware do not provide sufficient support for web application deployment. In particular the GUI widgets for uploading and downloading of PDFs file are not available. Undeterred I turn to Pyscript to see if I can code up a minimalist web applications in another weekend. I was fairly pleased with the result of a weekend worth of work. It is bare minimal as I have very limited knowledge of CSS and html. But the PDF processing works and anyone can visit the website @ <a href="https://chenkianwee.github.io/pdfautomated" target="_blank">PdfAutomated webapp</a> and process their PDFs. The whole project is hosted on <a href="https://github.com/chenkianwee/pdfautomated" target="_blank">my github repository here</a>.

![image-title-here](/images/blogs/app/pdfautomated_webapp.png){:class="img-responsive"}

# Conclusion
I was able to develop a PDF processing program for both Ubuntu and Windows OS and a minimal frontend web application for the browser over two weekends. Beeware and Pyscript have massively streamline the distribuition and deployment of Python programs. These tools look very promising as there are still in early developmental stages. Framework like Beeware and Pyscript will become more accessible with the increasing use of Large Language Models (LLMs) like chatgpt (which I have used for developing the application). We can easily learn and get support from LLMs in the application development process. I look forward to developing more project-specific single-task applications with these tools so that my colleagues can go home early with the lessen workload. I hope this post provides you some insights on the issue. What are your thoughts? <a href="https://www.linkedin.com/posts/kian-wee-chen-79b2b721_python-beeware-pyscript-activity-7360522919862542336--tpF?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAR-VqcBI2WVhLSf-dcz1wsslwv9rVp1vYE" target="_blank">Let’s continue the conversation in the comments</a>!

