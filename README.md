# Cloud-Native-Podcast

## Title: Decoding Platform Engineering: Build vs Buy Dilemma - [Episode 84](https://youtube.com/live/c2r3IeS7O4I)

## Speakers Intro: 

[Michel Murabito](https://twitter.com/michelmurabito) Currently holding the position of Developer Advocate at [Mia-Platform](https://mia-platform.eu/), he began writing software for fun at the age of 12. He landed his first job at 18 as a Software Developer, and from there, he started exploring various contexts and new opportunities for professional growth. He worked as an employee and a freelancer, collaborating on several technological projects for the Sicilian Region, MiBACT (Italian Ministry of Cultural Heritage), and numerous digital startups and innovative products for large international clients. Among his greatest passions is sharing new technologies and how developers can help create better products; between 2021 and 2022, he participated as a speaker in 60 events and conferences in Italy and Europe. He has started publishing content on these topics on the YouTube channel DevelopersLife, which now has 2500 subscribers and a community of over 550 members behind it. 

[Rhea Arora](https://www.linkedin.com/in/rhea-arora/) With a Bachelor's in Software Engineering and a Master's in Strategic Marketing, Rhea has a strong technical background coupled with 2+ years of experience working as a DevRel at different tech companies. She loves traveling, trying new cuisines, and showering love on every dog she sees.

### Episode 84 - 27th July 2023 
#### **Intro of the episode**, 
Platform engineers play a crucial role in designing, building, and maintaining the platforms that enable efficient and scalable software development and operations, but there are possibilities where could a message go possibly wrong in PE hype, In this episode, we unravel the complexities that platform engineering teams face when deciding between buying pre-built solutions and building custom in-house platform. Join me in welcoming Rhea Aroara Dev Rel at Mia Platform and Michel Murabito DA of Miaplatform as we engage, for an enriching episode on the "Buy vs. Build Dilemma in Platform Engineering." Gain a clearer vision and embark on a path that aligns with your organization's goals.


### **The current state of development (volatile market, the surge of tools (refer to the CNCF landscape))**
**[Rhea Arora](https://www.linkedin.com/in/rhea-arora/):**  The technology landscape is constantly evolving, and new tools and frameworks are being developed to address various challenges in software development, cloud infrastructure, and data management. This includes tools like Docker, Kubernetes, AWS Lambda (and in general serverless), and CI/CD (Continuous Integration/Continuous Deployment) pipelines. Developers and DevOps teams are continually exploring and adopting these tools to streamline development processes, enhance scalability, improve security, and reduce operational overhead. The rise of microservices architecture has also driven the need for tools that enable seamless communication and coordination between various microservices. As we speak about Cloud native services we can also discuss CNCF which is the Cloud Native Computing Foundation. 

The CNCF, founded in 2015, is a vendor-neutral organization that aims to promote and foster the adoption of cloud-native technologies. It hosts a vast ecosystem of open-source projects, including some of the most popular ones like Kubernetes, Prometheus, Envoy, and many many many others. These projects cover various aspects of cloud-native computing, such as container runtimes, service mesh, logging, monitoring, and more.

As the CNCF landscape continues to grow, some tools are added to it and other tools keep changing and upgrading over time,  it becomes essential for organizations to navigate this vast ecosystem effectively. CNCF projects often serve as the foundation for cloud-native applications, and understanding their capabilities and integration points is crucial for modern software development and infrastructure management. 

In today's fast-paced tech landscape, startups often face the challenge of selecting the right tools from the CNCF ecosystem. When we talk about tools, we have so many options for tasks, for example, if we look at API gateways, finding the perfect fit can be overwhelming and time-consuming. Sometimes, starting from scratch seems like the only option for specific functionalities, making software reuse a real challenge. But of course, in any case, it depends… Maybe starting from scratch is a better option, but more on this later where we will discuss other important considerations to keep in mind.

The market demands change rapidly, and for startups, keeping up with these shifts is crucial. They need to be agile and able to integrate existing systems seamlessly to stay competitive. However, this can be a daunting task that might delay their time-to-market.

That's where platform engineering comes in as a valuable solution. It could offer a ready-to-use ecosystem with tools and configurations that allow startups to focus on their core business code without getting bogged down by complex setup requirements. Platform engineering gives them the flexibility to choose and easily switch between different tools, such as mentioned before - API gateways, based on their strategies and needs.

**[Saim](https://twitter.com/cloudnativeboy):** Stay updated with industry trends, Leverage community-supported tools, Evaluate tool maturity and stability, Embrace interoperability and standardization, Conduct thorough evaluations, Foster a culture of experimentation. The key is to carefully evaluate, experiment, and adapt to the changing development landscape based on your organization's specific needs and goals. Regularly reassess your tooling choices to ensure they align with market trends, industry best practices, and your long-term development strategies 

---

### **Introduction to platform engineering (explaining what it is and its advantages)**
**[Rhea Arora](https://www.linkedin.com/in/rhea-arora/):** 
-   Let’s begin with ***what Platform Engineering*** really is: Platform engineering is the practice of creating a robust and scalable foundation, or platform, that enables efficient software development, integration, and deployment. It aims to simplify complex technical tasks, accelerate development processes, and facilitate the seamless integration of various technologies, ultimately empowering developers to focus on building high-quality applications and services and leaving out repetitive tasks that are pre-built.

-   Platform engineering encompasses various aspects, such as creating and managing containerized environments, setting up continuous integration and continuous deployment, helping you to implement automated testing, and ensuring efficient monitoring and logging. 

-   The platform serves as a stable and consistent environment for developers to build, test, and deploy their code. It establishes best practices, guidelines, and common patterns that ensure consistency across different projects, different teams, and people. By creating this standardized foundation, platform engineering promotes collaboration, enables faster onboarding of new team members, and reduces the time spent on repetitive setup tasks.

**[Saim](https://twitter.com/cloudnativeboy):** While a chat with. [Alexis](https://twitter.com/monadic), I really like the way he defines [Platform Engineering](https://www.youtube.com/watch?v=p6D-NYkVp9E) is how we simplify computing for every developer in our Organization by creating the environment for them to run their apps those environments are the platform and the job of the platform team is to choose how they are built and where they run and make sure they're always available in an easy way and separating those concerns b/w the automated platform and app devs who have an easy time that is Platform Engineering. 

---

### **What were the driving factors that led to the emergence of platform engineering as a distinct discipline within software development?**
**[Rhea Arora](https://www.linkedin.com/in/rhea-arora/):** ***Platform engineering emerged as a distinct discipline within software development due to several driving factors***. 
-   First, the rapid pace of the market demanded faster delivery of software functionalities to meet business requirements. Without platform engineering, developers spent significant time configuring various tools, slowing down the development process. 

-   Second, the shift to microservices in large companies led to multiple teams working in parallel with different languages and approaches, resulting in duplicated efforts and inefficiencies. 

-   Third, centralizing technology information and documentation was challenging and expensive, making it difficult for developers to access critical resources. Lastly, onboarding new employees required extensive tutoring to understand the company's complex platforms and find relevant documentation. In response to these challenges, platform engineering emerged to simplify developer work, streamline processes, foster collaboration, and provide a cohesive foundation, like a superhero toolkit, to enhance software development efficiency and effectiveness.

**[Saim](https://twitter.com/cloudnativeboy):** The advent of cloud computing and Infrastructure as Code (IaC),  DevOps and Continuous Delivery, Increasing Complexity and Scale, Need for Standardization and Efficiency, With the growing importance of observability and monitoring, The rise of containerization technologies like Docker and like Kubernetes contributed to the need for platform engineering.  
 
---

### **Architecture and Design Considerations for Platform Engineering Teams.**
#### **How do you approach designing a scalable and resilient platform architecture that can handle increased user demand and growth over time?**
**[Michel](https://twitter.com/michelmurabito):**

#### Keywords: 
-   **Different entities:** platform engineering team, consumers, and contributors.
-   **Flexible system:** adding, removing, modifying tools, and components easily.
-   **Transparency:** changes should not affect users.

- The best idea from my point of view is to have 3 different entities. Of course the platform engineering team, they are responsible for the platform, making and checking standards, to inform and share common knowledge. They will provide new global functionality, work on the infrastructure (to increase and optimize them) and of course, do be a bridge between the different teams. (like the producers and the consumers). We can imagine this as an open-source organization (where someone uses the OSS, others will contribute to improving the OSS and a central team are the main contributor)
- This kind of system needs to be very flexible, you can add/remove/modify tools, components, and other parts in an easy way. That means if you have to add a new tool (and when we talk about tools we can talk also about infrastructure and so on) because you need it, you will do that without changing the platform and of course in a transparent way for the users (developer)

**[Saim](https://twitter.com/cloudnativeboy):** Horizontal scalability is achieved through the deployment of multiple instances of your application and services, allowing you to distribute the workload across different nodes or containers. This ensures that as user demand increases, we can dynamically add more resources to handle the load, achieving optimal performance without any service interruptions. Prioritize continuous integration and continuous deployment (CI/CD) practices to ensure rapid, reliable, and safe updates to your platform. Monitoring and observability play a vital role in maintaining a resilient platform. Integrate robust monitoring tools to gain insights into system health and performance. This proactive approach allows you to detect anomalies, bottlenecks, or performance degradation, allowing you to take timely corrective actions and prevent service disruptions.

---

#### **What are the key considerations when it comes to selecting technologies, frameworks, and tools for your platform engineering architecture? How do you evaluate and choose the right ones?**
**[Michel](https://twitter.com/michelmurabito):**

#### Keywords: 
-   Critical selection if building from scratch.
-   Three metrics for tool choice: integration, maintenance and support, necessity.
-   If the platform is not your core business, consider using a platform builder like [Mia-Platform](https://twitter.com/MiaPlatform).

If you start to build your platform from scratch you need to pay a lot of attention to the choices. I think that depends, but my idea to start this kind of challenge is to start small and try to improve/increase. But from my point of view if the platform isn’t your core business bay it remains the best solution.

But if you want to make it from scratch my first suggestion it’s find the right tool. In my case to choose a tool I will use 3 metrics. 1) the tool is easy to integrate into my system? 2) the tool it’s maintained and in case of a problem I can ask for paid support? 3) Do I need the tool? I can continue without including it. 

Of course, if the platform isn’t your business (but you will use the platform to increase your business) my primary suggestion is to find a good platform, like a Platform Builder. Choose it if the y has the major functionality that you need, if is updated frequently, and if contains the plugin useful to you. Another important point is to make sure the platform builder can offer you support and has a team on hand to help with any changes you require or errors. regarding the support (maybe it’s important to have enterprise support). For example, Mia-Platform can provide enterprise support level, and there is a lot of plugin and integration ready to use and a lot of integrations with providers (like git, pipelines, cluster, and so on)
 
**[Saim](https://twitter.com/cloudnativeboy):** 
-   **Business Objectives and Requirements:** Start by understanding your organization's business objectives and platform requirements. Identify the specific challenges you aim to address, the scalability needed, and any unique features required for your platform.

-   **Scalability and Performance:** Assess the scalability and performance capabilities of the technologies and tools you are considering. Look for solutions that can handle current and future growth, as well as accommodate spikes in demand.

Structured approach and considering these key considerations, you can confidently select technologies, frameworks, and tools that form a solid foundation for your platform engineering architecture, enabling you to build scalable, robust, and successful platforms.  
 
---

### **Forward-thinking with Platform Engineering?**
#### **How do you address the challenges of platform evolution and backward compatibility?** 
**[Michel](https://twitter.com/michelmurabito):**

#### Keywords: 
- Use of standard configurations.
- Regular updates to mitigate breaking changes.
- Standard tool integration via APIs.

A good platform doesn't reinvent anything, the idea is to use standard configuration (for eg). Of course, sometimes can be exist breaking changes but in the majority of cases you can update versions without changing code.

Of course, if Kubernetes (just an example) introduce in the new version braking changes you will update the platform to adapt it to the new stuff, but if you use kubernetes without any platform (and there is a braking changes) in any case you need to update manually it. But the idea it’s try to update each version whenis possible (in this way it’s more easy in future update in case of breaking changes).

Pay attention to include tools in  a standard way, using api for eg (in this way you can remove a tool and use another one if necessary without lot of works)
Breaking change - when you change from one version to another and the old version doesnt work anymore.

---

#### **How do platform engineering teams collaborate with other teams, such as product management and software development, to ensure alignment and a shared vision for future platform enhancements and features?**

**[Michel](https://twitter.com/michelmurabito):** 
#### Keywords: 
-   Prioritizing features based on business needs.
-   Cross-team collaboration to prepare the roadmap.
-   Platform engineering team acting as an "orchestra conductor".
-   Contributions and maintenance of software included in the platform.

It’s like other problem related to the software engineering. There is 2 type of necessity, the real priority and the others. When you plan new features you need to keep in mind about business requirements, cost (to developer the new functionality) and risk to include it in your software. 

At the end the important things about that is to try to find the best solution for the company. In this context the platform engineering team need to prioritize the feature roadmap talking with any other team. After that they (with other key figure, like the CTO) can prepare a roadmap.

About the collaboration, the PE team there is like a “conductor” of an orchestra, the need to understand all the necessity from different teams and after that choose the right roadmap and direction (the right roadmap, priority etc) for the whole company. 

About the components or the independent software included in the platform, of course if the code it’s from the company the platform engineering team can operate like a maintainer, they can accept contribution and they can approve that. In this case a real urgent feature can be implemented by the team that ask the feature in autonomous way. It’s like a big open source project.


**[Saim](https://twitter.com/cloudnativeboy):**  Platform teams should be careful to not open up their codebase to external contributions without making some thoughtful investments to support those contributions. There can be deep frustration all around if a platform team proudly proclaims in an all-hands that their codebase is a shared resource, but then find themselves repeatedly telling contributors from other teams "No, no, not like THAT!".

**Key takeaways:** A platform team succeeds on the back of collaboration with other teams, and that collaboration can take many forms. Choosing the right form involves considering the type of platform work the other team is doing.

---

### **Drive a Culture of Kubernetes Standards With Platform Engineering.**
#### **How can platform engineering teams showcase the value and impact of Kubernetes standards to key stakeholders and decision-makers?**

**[Michel](https://twitter.com/michelmurabito):** 
#### Keywords: 
-   Standardization of development practices.
-   Scalability and cost optimization.
-   Portability across cloud providers.
-   Automation and efficiency (e.g., environment creation).
-   Energy and cost savings (e.g., kube-green).

About this point there is a lot to talk. If you start to use a IDP (for eg) youcan put in place standards for developers and other tech people. That means that the whole company will write software with same standards, this is important because for example change team inside the company can be more easy (if all the company use the same standards to work).

Use the right approach can help to scale application in the right way and if the business grow also the application can grow (and of course if the business decline also the application (and the infrastructure can decline)). Using standards is more easy to predict costs and optimize them.

Using kubernetes you can move your infrastructure to and cloud provider to another one (without change nothing), in this case you can use the more convenient infrastructure (and of course save money). (if you use custom staff can be hard change provider).

A couple of day ago i talked with a developer in a big company, and he say that for create a new environment for test can use also 2 o 3 days of works (it’s incredible), with an IDP the developer can create the environment in 10 seconds (if he have the permission/privileges), without open assistance ticket and in a self service way. This is possible because the PE team automatize all the procedure to do that, but in this way is easy to demonstrate more efficiency.

You can also put in place systems to switch off the development environment during the night, the weekend and so on. Today you can do that with kube-green. How many money can you save with this simple approach? You can measure it in a easy way. And you know when you talk with manager, c-level etc the more important point is about number and of course money.

---

#### **What metrics or success stories can be used to demonstrate the benefits of standardized Kubernetes deployments?**
**[Michel](https://twitter.com/michelmurabito):** 

#### Keywords:
-   Time to get a new environment.
-   Deployment frequency.
-   Time for onboarding new team members.
-   Reduction of time spent on sideline activities.

The story that we talk before 2 days vs 10 seconds to have a new environment it’s an example. We can talk about deploy frequency, time to have new environment, time to onboarding new people are just example. There is a lot of metrics, but in any case each metrics are relevant in a specific context. For me (for eg) can be mandatory reduce the time to have a new environment, maybe for you can be the number of release x day and so on.

If we talk about metrics i thinks that the most important metric for the developer are the time used for sideline activity (a developer want write code and not watch systems, wait for env, or so on). For a manager this improvement can be related to the time to market. If the developer can start to write code from day 0 he can be more productive and of course produce better code, better documentation and so on. For the manager this kind of benefic can be translate into save money, have a more fast company and more happy employees.

--- 
 
#### **How to begin with Platform Engineering?**
**[Michel](https://twitter.com/michelmurabito):** 
#### Keywords: 
-   Mindset preparation: it's not just a project, it's a path.
-   Introduction of standards and automations.
-   Starting with basic projects and small functionalities.
-   Flexibility to improve and introduce new features.

Maybe start the activity can be hard, put in place all the minimum feature to start with PE can be hard, we talk a lot about this in the Mia-Platform Blog (we have a lot of articles vendor neutral on these topics). 

To start maybe the first step it’s be aware that isn’t just “a project” is a path. You can start with PE just introducing in the company standards, put in place first automations and so on. Of course if you want to have the perfect IDP writted in 5 days maybe you will understand that isn’t possible. Also if you decide to buy a ready solution your organization need time to understand the benefit and to improve processes. At the end today we talked about technology but from my point of view isn’t just about technology it’s more related with people.

Another suggestion is to start from the basics, just small projects, a couple of functionalities, just to try. If work you can improve, introduce new stuff, improve the existing and so on.
 
---  

#### **The decisions between building products and buying them (weighing up the tradeoffs)** 
**[Rhea Arora](https://www.linkedin.com/in/rhea-arora/):**
-   Building an IDP solution from scratch can be challenging, as it requires careful step-by-step development, and it can become costly. Opting for a ready-to-use IDP solution offers significant advantages, saving time and effort in building and managing the platform. Existing IDPs come packed with a wealth of functionalities, plugins, and connectors from day zero, making it easy to integrate with various services. For example, Mia-Platform is an IDP builder that provides a comprehensive set of tools and functionalities, supporting multiple cloud providers, Git repositories, and pipeline runners, simplifying the process significantly.

-   However, if you need a highly personalized IDP tailored precisely to your specific needs, building an internal IDP might be the better fit. It allows you to customize every aspect of the IDP according to your requirements, providing a perfect solution for your product. The trade-off is that building an internal IDP will require time, effort, skills, and ongoing maintenance, which can be a burden for developers. And in many cases it's not worth it if it's not part of your business, but just a tool to do your business

-   On the other hand, buying a ready-to-use IDP offers instant solutions with a low time-to-market. Updates are automatically provided by the IDP creators, continuously improving technologies and features. This variety of features allows you to choose and utilize the functionalities that best suit your needs without the hassle of building them from scratch. Of course, if you buy an IDP maybe there are ways to add new custom functionality. Maybe isn't easy like your own IDP, but there can be a way to start very fast and integrate new functionalities.

-   Ultimately, the decision to build or buy an IDP depends on your specific requirements, budget, skills, and timeline.

**[Saim](https://twitter.com/cloudnativeboy):** 
-   **Key takeaways:**
    Evaluate the core competency, Seek input from stakeholders, Consider time-to-market, Analyze customization needs, Assess cost implications, Evaluate available solutions, Consider strategic partnerships, Weigh technical expertise, Consider long-term sustainability, Analyze risks and dependencies, Seek input from stakeholders, there’s no one size fit’s all the decision between building and buying is highly context-specific. Analyze your organization's unique needs, resources, and constraints to determine the best approach. It's also worth considering a hybrid approach that combines building and buying to strike a balance between customization and efficiency.

---  

### **Concluding Thoughts and key takeaways**
**[Rhea Arora](https://www.linkedin.com/in/rhea-arora/):**
In conclusion, platform engineering plays a vital role in modern software development by simplifying complex processes, streamlining workflows, and empowering developers to focus on building innovative applications. The use of an internal developer platform makes perfect sense due to its numerous advantages. By providing a tailor-made solution, an internal platform ensures that features and functionalities align precisely with the organization's unique requirements, leading to a more efficient development process. Additionally, it enables customization and personalization of every aspect of the platform, promoting flexibility and adaptability as business needs evolve. Moreover, the internal platform reduces time-to-market significantly, as it offers instant solutions and pre-built tools, accelerating application delivery. Ultimately, embracing platform engineering and adopting an internal developer platform not only enhances developer productivity but also facilitates better collaboration, cost-effectiveness, and a competitive edge in today's fast-paced technological landscape.

**[Michel](https://twitter.com/michelmurabito):** 
#### Keywords:
-   **People-centric approach:** The importance of individuals in navigating technological changes.
-   **Technological revolution:** The human impact in shifts like adopting Kubernetes or platform engineering.
-   **Team collaboration:** Cooperation among diverse teams for optimal platform engineering.
-   **Value creation:** Effective technology management for business growth hinging on competent, motivated people.

In conclusion, despite the advanced technologies and innovations we have discussed, the most critical element to consider is people. In building a resilient and scalable platform architecture, in the evolution and implementation of standards like Kubernetes, at the center of every decision and strategy is the individual. In every technological revolution, humanity must take center stage. This is particularly true for platform engineering, where the ultimate goal is to facilitate the work of development teams, improve efficiency, and foster innovation. We must remember that technologies are merely tools in people's hands, tools that can be used to create value and grow business only if managed correctly. Therefore, the real challenge is to train competent and motivated teams that can collaborate effectively to make the most of these resources and guide the organization towards success.


**[Saim](https://twitter.com/cloudnativeboy):** 
-   **Key takeaways:**
    -   **How to look at the platform:** There is no one-size-fits all approach to platform engineering. It boils down to each organization’s specific requirements, priorities and what they want to accomplish via a platform. The platform is not just an IDP or a Backstage deployment or a self-serve portal. Developers are not necessarily the only users of the platform. Platform teams must thoroughly understand all of their internal user personas, and their needs, and develop the right kind of backend and user interfaces for the platform that delivers maximum value to all their internal users.
    -   **Success of the platform team hides in:** Effective collaboration, communication, leadership skills to guide teams, make strategic decisions, manages resources effectively, and drive project to succes are key skills that platform engineers should possess or adhering to.
    -   **What should a platform processes?** A platform should processes capabilities include and not limited to standardized automation, consistent security policies, unified Kubernetes bimodal multitenancy, access management and a single administration pane, offering visibility for the entire infrastructure spanning multiple clouds. 

---  

## Platform Engineering:

### Learning resources - Videos
►  [Platform Engineering How Did We Get Here | Ep 81](https://www.youtube.com/watch?v=p6D-NYkVp9E)

►  [Introduction to platform engineering with Backstage | Episode 70]( https://www.youtube.com/watch?v=Pw01NqvXctQ&t=3473s)

►  [Success Metrics for Platform and Platform Teams | Ep 80](https://www.youtube.com/watch?v=CDadi--MqvY&t=2007s)

►  [Intro for Stress Less Platform Engineering](https://www.youtube.com/watch?v=FSJrePkxKBQ)

►  [Dave Reacts To Platform Engineering HYPE  @ContinuousDelivery](https://www.youtube.com/watch?v=wXyNHngEN-s&t=2s)

►  [DevOps vs SRE vs Platform Engineering | Clear Big Misconceptions  @ByteByteGo](https://www.youtube.com/watch?v=an8SrFtJBdM) 

►  [Platform Engineering as a (Community) Service   @GOTO-](https://www.youtube.com/watch?v=4N2ywun-wTE&t=3s)

►  [Enable secure self-service access to Kubernetes clusters with Paralu  @PlatformEngineering](https://www.youtube.com/watch?v=UbLnCGOv0Rk&t=143s)

---  

### Articles:

►  [How platform teams get stuff done](https://martinfowler.com/articles/platform-teams-stuff-done.html)

►  [How To Empower Modern Kubernetes Management With A Platform Team Model](https://www.forbes.com/sites/forbestechcouncil/2023/02/23/how-to-empower-modern-kubernetes-management-with-a-platform-team-model/?sh=961fde252c72)

►  [SRE vs. DevOps vs. Platform Engineering](https://thenewstack.io/rafay-backstage-plugins-simplify-kubernetes-deployments/)

►  [Architecture and Design Considerations for Platform Engineering Teams](https://thenewstack.io/platform-engineering/architecture-and-design-considerations-for-platform-engineering-teams/)

►  [PRODUCT VS PLATFORM ENGINEERING – RISE OF PLATFORM ENGINEERING, TEAM STRUCTURE, PRINCIPLES & PRACTICES](https://www.sonata-software.com/blog/product-vs-platform-engineering-rise-platform-engineering-team-structure-principles-practices) 

►   [CNCF Platforms White Paper](https://tag-app-delivery.cncf.io/whitepapers/platforms/)

►   [Platform Engineering: Challenges and Solutions](https://www.cloudknit.io/blog/platform-engineering-challenges-and-solutions) 

►   [Platform Engineering: Using it to Gain Competitive Advantage](https://www.cloudknit.io/blog/platform-engineering)

►   [PlatformCon 2023: Bigger and Even Better](https://thenewstack.io/platformcon-2023-bigger-and-even-better/)

►   [6 best practices to keep Kubernetes costs under control](https://www.infoworld.com/article/3700775/6-best-practices-to-keep-kubernetes-costs-under-control.amp.html) 

--- 

###  🛠️  About Miaplatform 🛠️  
Build your Internal Developer Platform (IDP), self-serve developers, and ship applications faster. 
-   🌎   https://mia-platform.eu/
-   🔔   https://twitter.com/MiaPlatform

--- 

### 👋 Contact me 👋 
-   https://twitter.com/cloudnativeboy
-   https://www.linkedin.com/in/saim-safder/ 
 
 



 

 

