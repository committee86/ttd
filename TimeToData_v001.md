# What is Time to Data (TTD)

Time to Data shows how much time end user requires to start using data asset in their specific use case.

Time to Data (TTD) is an integral metric (like processing SLA or end-to-end latency) and it reflects on the experience of the end user of data. This metric is calculated from the moment end user identified the need in certain data (prior to initial research on what data is available) to the moment data asset is incorporated into the end user use case (application, report, script, notebook, etc.)

By the end user of data, I mean a person or a process which requires some particular data asset to perform certain tasks. It may be a business user, developer, data scientist or any other role within the organization.

By the data asset I mean any physical piece of data (file, table, etc.), knowledge (text, algorithm, etc.), information (conclusion, insight, etc.) or a process (pipeline, script, program, model) which can be consumed digitally (via application or process).

# Why do we need Time to Data?

Currently our organizations do have this metric, but they use it implicitly. A large number of the Data Transformation discussions start with the business users complaining on the time required to get access to the data they are interested in. I had numerous cases over the last decades with claims like “I have to wait many weeks before I can use this data in my report”.

We need, however, to be cognizant of the fact that “getting access to data” may imply different things like, for example, identifying if such data asset exists in the company, acquiring data in case it is not available, improving data processing and quality to the acceptable values, provisioning infrastructure and access to the existing data. 

Having Time to Data as an explicit metric may help us to improve overall experience of our business users.

First and foremost, we could identify major bottlenecks and delays impacting our end users experience so we can prioritize the most critical tasks impacting overall TTD. Such bottlenecks can be found in the lack of tools or quality of metadata or complexity and inefficiency of the process. Good thing is that we can make it clear where the improvements are required.

Secondly, such a metric focuses directly on the end user experience and ensures critical tasks for our end users are addressed first. So, we can establish and control user-centric approach.

Such a metric (when combined with other data-related metrics) can be used to motivate data producers to move quicker and focus more on the needs of their end users. It may also help to establish a good balance between data housekeeping tasks (such as data quality, data security, etc.) and tasks related directly on using data for achieving business results.

## Word of Caution: Tasks are Not Equal

I have to say it out loud here. Any metric can be misused. Especially success rates which are time bounded. We tend to treat almost all our tasks as urgent thus some level of misuse or abuse of metric as Time to Data can be foreseen.

To protect against such a misuse of the metric and reduce the pressure on the data teams to acceptable values I can recommend several approaches.

1.        In order to assign Time to Data for a particular set of tasks, they should be considered as a high priority for the business (preparing for large-scale event, performing audit, compiling mandatory reports to the regulators, etc.) Prioritization of tasks should follow well-defined framework, so no minor tasks demand low Time to Data.

2.        For the entire organization or large group of tasks Time to Data can be only used as a relative parameter (decreasing / increasing in percentage in various line of businesses or sets of scenarios).

## Word of Caution: Data Quality

Leaning on TTD doesn’t mean that we must compromise Data Quality. This means that the two should be linked together and be in balance. Business needs data as soon as it is possible but:

    From one side business needs data which is as accurate as possible and Data Quality metrics help to ensure this. At the same time Data Quality cannot serve as an excuse for not being able to deliver data to the business by the deadline.
    On another hand, Data Quality is not the only thing which affects Time to Data – some processes (like access granting), lack of tools (poor Data Catalogues, for instance), infrastructure issues (long time for resource provisioning), etc. can have much stronger impact on time to data.

To link the two, we could use existing Data Quality SLAs as an input to Time to Data measurements. Meaning that TTD will be measured until the Data Quality metrics are in-line with the business expectations.

## Word of Caution: Data Engineering

In this document Time to Data is defined as time end user requires to start using data asset in their specific use case.

Such definition doesn’t only cover technical details for Time to Data but also implies the amount of time end user must spend trying to understand data itself, access tools and methods (such as SDKs, libraries, etc.)

This interpretation of TTD allows us to put quality of documentation, metadata, additional data parameters as well as quality of supplementary code under control. It also allows us to indirectly influence standardization of organization technology portfolio via skills dependencies.

# How to Measure Time to Data

Before we begin talking on how we can measure Time to Data let us recap what is the scope of this metric.

## Scope of Time to Data

As discussed above, scope of Time to Data might be slightly different based on the scenarios we are talking about (If this is a new (non-existing) or already existing asset).

Thus, I can define scope of the Time to Data as follows.
! Image

Thus, Time to Data covers an entire provisioning lifecycle for new and existing assets including all the Data Engineering and Data Quality tasks as well as time for integrating data asset into business use case.

As you may observe, there is an excessive scope for Time to Data. Main reason for this is that we would like to cover our TTD end-to-end across all the processes and LOBs so we can understand where main bottlenecks and obstacles actually are.

Obviously, such a huge scope causes some complexities on measuring TTD. There are two main approaches to measure TTD and they can be used simultaneously.

- Direct Feedback Loop.
- Automatic Data Collection and TTD Measurement.

## Measuring Time to Data via Feedback Loop

First approach is to use Direct Feedback Loop. It may be done as a form to be filled after data asset is integrated into a business use case. Such a form may include entire scope of TTD and relative time parameters associated with each step.

Main issues with the direct feedback form are that it is not easy to enforce and if not enforced it (most probably) will have some strong tendency to be more negative and problem biased. It may be also affected by the inter-person communications and additional biases coming from internal organizational politics.

Nevertheless, direct feedback loop is a must have component as it ensures that the user-centric approach prevails.

## Automatic Measuring of Time to Data

Automatic Measuring of TTD may require quite some additional integrations and heavily depends on the existing processes within organizations.

Typically, main sources of information in such approaches will be formal ticketing system where users register tickets for data and security-related tasks. Such tasks should be linked together in the chain of tickets either by direct mention (like linked issues) or via the topic (like name of the datasets / requestor, etc).

It also should be taken into consideration which division or person was responsible for the ticket so you can link it later to the scope of TTD and your existing data environment. In case of the marketplace-style solutions this can be achieved by parsing marketplace logs.

In situations when no ticketing system is available, and all the communications are performed via emails organizations can implement a separate simple taxonomy for an emails topic so these can be chained and analysed later by email parsers.

In general, such a task can be implemented with some basic automation tools either for a ticketing system or email parsers.
Word of Caution: Missing Data

Obviously, if we rely on topics and links some of those might be missing. It is also obvious that it might not be easy to link this data and process after the fact. This is where direct feedback may act as a verification tool and as a source for additional information.

The nature of Time to Data doesn’t require perfectly collected data points though, as it is not an investigation tool rather than a directional metric for useability and effectiveness of data management within the company.

## Word of Caution: Data Environment Map

Root cause analysis and discovering bottlenecks may become more efficient in case processes and data ecosystem is described in a form of a single consumable artifact. Such an artifact is usually a diagram showcasing dependencies between components and link between processes and components tailored to the specific use case of provisioning access to an existing or a new data asset.

Such a map can be created for an entire organization and separately (if required) for high-priority tasks / users.

# How can we use Time to Data to enforce constant improvement?

Frankly, there is no need in collecting any metrics if you are not planning to act on those. So, how you can (potentially) use Time to Data to make substantial improvements in your data ecosystem.

Process to take actions on the TTD may look pretty similar to any iterative improvement process.

1. Implement basic TTD monitoring solution (either direct feedback or some simple automation).
2. Measure Time to Data and map it onto the overall Data Environment Map.
3. Identify bottlenecks and obstacles and assess complexity of changes.
4. Perform prioritization of changes.
5. Plan and implement changes.
6. Extend / improve TTD monitoring and reiterate.

Obviously, there should be a motivation for performing changes based on measured TTD.

As any new thing, Time to Data must be explained, promoted and battle-tested in the organization. It also should be an iterative process starting with some (relatively) small scope. After the initial tests and proof of value it can be extended further.

I would not recommend enforcing TTD at this moment as it will be more useful as an indication metric and vehicle for general improvement of UX. 