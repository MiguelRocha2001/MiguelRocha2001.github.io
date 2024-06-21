---
title: "SpecialVFX@Cloud"  
excerpt: "Welcome to SpecialVFX@Cloud, a scalable cloud solution for special effects processing, developed as an IST Cloud Computing project."  
header:  
  image: /assets/images/12071207_SL-101820-36860-19.jpg  
  teaser: assets/images/12071207_SL-101820-36860-19.jpg  
sidebar:  
  - title: "Responsibilities"
    text: "Developer, Designer"
    image: /assets/images/kisspng-cloud-computing-information-technology-computer-ic-cloud-filled-outline-icon-5ce78cd7c12c50.0563520515586787437912.pngre
    image_alt: "Cloud logo"  
gallery:  
  - url: /assets/images/architecture-diagram.jpg  
    image_path: assets/images/architecture-diagram.jpg  
    alt: "SpecialVFX@Cloud system architecture"  
---

Welcome to SpecialVFX@Cloud, a scalable cloud solution for special effects processing, developed as part of an IST Cloud Computing project by [Miguel Rocha](https://github.com/MiguelRocha2001), [Lucas Pinto](https://github.com/luckspt), and [Kenneth Brattli](https://github.com/kennethbrattli).

**Project Description:**

SpecialVFX@Cloud is a service hosted on Amazon Web Services (AWS), designed to support a hypothetical special effects studio by executing computationally-intensive tasks. The main functionalities include:

- **RenderImage:** Generate photo-realistic images using ray-tracing.
- **BlurImage:** Apply a blurring effect to images.
- **EnhanceImage:** Highlight edges in images to enhance details.

**Goals:**

The primary goals of this project were to:

1. **Implement Elastic Scalability:** Ensure the system can automatically scale by increasing or decreasing the number of workers based on the number and complexity of user requests.
2. **Optimize Cost Efficiency:** Balance between cost and performance using a mix of EC2 instances and Lambda functions.
3. **Collect Performance Metrics:** Instrument the application to measure the complexity of requests, aiding in load balancing and auto-scaling decisions.
4. **Utilize Cloud Environment:** Deploy the system on Amazon Web Services (AWS), including EC2 instances, Lambda functions, and DynamoDB for metrics storage.
5. **Automate Deployments:** Automate all cloud deployments and ensure resources are efficiently managed and deleted after use.

**Overall Workflow:**

1. **Load Balancer (LB):** The entry point of the system that receives all web requests and forwards them to either an EC2 instance or a Lambda function based on estimated request complexity.
2. **Workers:** Execute the requested operations. These are of two types:
  - **VM Workers (EC2 Instances):** Handle requests directly and can be instrumented to collect performance metrics.
  - **FaaS Workers (Lambda Functions):** Handle requests with fast startup times but higher cost per request.
3. **Auto-Scaler (AS):** Monitors system performance and adjusts the number of active EC2 instances to balance load and cost.
4. **Metrics Storage System (MSS):** Uses Amazon DynamoDB to store performance metrics, aiding in decision-making for load balancing and auto-scaling.

**Milestones:**
- **May 17th: Project Checkpoint (Optional):** Submit your initial implementation and receive feedback on your progress.
- **May 31st: Project Submission:** Submit your fully functional system along with a final report.

**Documentation:**
- Check the project description [here](/assets/documents/CNV-23-24-project.pdf);
- The final report can be found [here](/assets/documents/CNV_G35.pdf).

**Useful links:**
- Github Source code [here](https://github.com/MiguelRocha2001/SpecialVFX-Cloud);
- Git-Lab Source code [here](https://gitlab.rnl.tecnico.ulisboa.pt/cnv/cnv24-groups/cnv24-g35/-/tree/master/infra?ref_type=heads).

---