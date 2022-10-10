# Karmada 2022 Annual Review

## Background

Karmada (Kubernetes Armada) is a Kubernetes management system that enables you to run your cloud-native applications across multiple Kubernetes clusters and clouds, with no changes to your applications. By speaking Kubernetes-native APIs and providing advanced scheduling capabilities, Karmada enables truly open, multi-cloud Kubernetes.

Karmada aims to provide turnkey automation for multi-cluster application management in multi-cloud and hybrid cloud scenarios, with key features such as centralized multi-cloud management, high availability, failure recovery, and traffic scheduling.

Karmada has built-in policy sets for multi-scenarios, enabling multi-dimensional and multi-level high-availability deployment of applications. At the same time, Karmada provides region-independent centralized cluster management, which solves the stickiness in business deployment.

The functionality and value of the Karmada project can be summarized at a very high level by these two main areas:

1. Provide a smooth evolution path for native Kubernetes, so that Karmada-based multi-cloud solutions can be seamlessly integrated into the cloud-native technology ecosystem, and provide enterprises with a smooth evolution solution from a single cluster to a multi-cloud architecture. 
2. Provide high-availability scheduling, failover, multi-cluster service discovery, multi-cloud cluster lifecycle management and other capability sets in a modular manner and 
   preset policy sets for a variety of typical user scenarios which allows users to freely customize the multi-cloud platform that suits them according to the actual situation of the enterprise.

### Sandbox Acceptance 

Karmada was proposed and accepted as a sandbox project in September 2021. ([GitHub](https://github.com/cncf/toc/issues/721)).

## Development metrics

In the past year, we joint effort with end users from multiple industries at birth and committed to building a more prosperous community.
We have held several meetups that allow us to communicate more directly with users and share some good practice cases. Also, we
continue to refine our documentation and usage examples so that our users can get started with our projects faster.

Also, we are open to integration of more CNCF projects including Envoy, Prometheus, Thanos, etc. We actively share our innovative ideas in the upstream community and drive standardization in the multi-cloud direction. 
Meanwhile, we continue to cooperate with projects in different fields, introducing amazing integration cases to their developers and users.

Through the above efforts, we have attracted a large number of developers and end users over the past year.
From the data we can clearly see this trend.

Specific devStats can be found [here](https://karmada.devstats.cncf.io/d/8/dashboards?orgId=1&refresh=15m).

Here are some links worth mentioning:

- [Stars and forks](https://karmada.devstats.cncf.io/d/3/stars-and-forks-by-repository?orgId=1)
- [Issues](https://karmada.devstats.cncf.io/d/12/issues-opened-closed-by-repository-group?orgId=1)
- [PRs](https://karmada.devstats.cncf.io/d/15/new-prs-in-repository-groups?orgId=1)

Karmada currently has [182](https://karmada.devstats.cncf.io/d/22/prs-authors-table?orgId=1) PR authors from [50](https://karmada.devstats.cncf.io/d/5/companies-table?orgId=1) companies.

The community has grown since the project entered the CNCF sandbox.

* We held bi-weekly community meetings constantly (total 38 times as of September 2022). The meeting records can be found in [here](https://docs.google.com/document/d/1y6YLVC-v7cmVAdbjedoyR5WL0-q45DBRXTvz5_I7bkA/edit). The average number of meeting attendees is around 25.
* Github stars increased from **1600+ to 2600+**
* Github forks increased from **200+ to 500+**
* Number of contributors increased to **[330+](https://karmada.devstats.cncf.io/d/18/overall-project-statistics-table?orgId=1&viewPanel=1)**.

[aaa](#Background)

## Maintainers

In the past year, we attach great importance to the development of developers.
We have established [the community membership roadmap](https://github.com/karmada-io/community/blob/main/community-membership.md). Based on this complete mechanism, developers can continue to grow while participating in the project.
We are actively involved in various open source events, such as Summer of Open Source and LFX membership, helping college students better grow in the open source community.

We have established a mature mentor system in the community.
With the help of our tutors, quite a few active and qualified contributors have been promoted to members or maintainers.

Compared with maintainers initially, Karmada currently has **7** maintainers from **4** different companies:

| Maintainer  | GitHub ID         | Affiliation | Email                    |
|-------------|-------------------|-------------|--------------------------|
| Hanbo Li    | @mrlihanbo        | Huawei      | <lihanbo2@huawei.com>    |
| Hongcai Ren | @RainbowMango     | Huawei      | <renhongcai@huawei.com>  |
| Kevin Wang  | @kevin-wangzefeng | Huawei      | <wangzefeng@huawei.com>  |
| Lei Xue     | @carmark          | Tencent     | <vfs@live.com>           |
| Shiyi Xie   | @GitHubxsy        | Huawei      | <xieshiyi1@huawei.com>   |
| Yifan Shen  | @zoroyouxi        | ICBC        | <shenyf@sdc.icbc.com.cn> |
| Yiheng Ci   | @lfbear           | VIPKID      | <ciyiheng@vipkid.com.cn> |

The full maintainer list can be found in our [GitHub repository](https://github.com/karmada-io/karmada/blob/master/MAINTAINERS.md).

## Adoption and Integration

In this section, we will discuss the progress on the project since being accepted into the Sandbox,
as well as specifics on adoption of Karmada in production environments and integration of ecosystem projects.

### Adoption

The biggest accomplishment from the Karmada community in the past year is the release of v1.0.0, the first major milestone in the project’s history, which was followed recently by even more improvements in v1.1.0, v1.2.0, and v1.3.0. With these versions of Karmada, the project is now stable and ready to be used in production scenarios. This is further validated by project adopters successfully running Karmada in production environments. 
Future enhancements and improvements are intended to be done in a backwards compatible way with a clear upgrade path. We do not anticipate any further breaking changes in subsequent minor and patch releases.

With Karmada reaching maturity, we are seeing end-users adopt Karmada and find success running it in their production environments. We consistently hear from users that have adopted Karmada as the core of multi-cloud and multi-cluster container orchestration engine to provide more efficient multi-cloud services within the enterprise. 
The community growth has been quite encouraging and we are pleased to be able to include specific details about some of their adoption success in the sections below.

Karmada now have 9 adopters that using Karmada in `production` environments. We just started to collect the adopters from last month, there are several other companies using Karmada,
but we don't have a public confirmation available yet. So the adopter list may grow over time. Some of these use cases are listed below.

* VIPKIP is an online English education platform which delivers 150 million training sessions across countries and regions. To provide better services, VIPKID deploys applications by region and close to teachers and trainees. 
  Therefore, VIPKID purchased dozens of clusters from multiple cloud providers around the world to build its internal infrastructure.
  How to manage multi-region and multi-vendor clusters has become a new challenge for VIPKID. By using Karmada, VIPKID gets the following benefits:
  (1) Higher deployment efficiency; (2) Differentiated control on applications; (3) Quick cluster startup and adaptation to GitOps; (4) Short reconstruction period and no impact on services.
* AIML INSTITUTE is a tech company that helps enterprises build integrated cloud native solutions for digital transformation.  Built on Kubernetes, their platform is cloud-vendor-independent. Customers can host service applications without regard for vendor differences. 
  However, their customers are demanding more and more on multi-cloud, and the scale and number of clusters and the O&M complexity grow sharply, they need to find a way to satisfy their customers. By using Karmada, existing resource definitions can be migrated into multi-cluster environment without modification.
  Based on Karmada's flexible expansion capabilities, AIML makes different tradeoffs and designs for different scenarios, and quickly builds their own multi-cloud container platform.
* Huawei Cloud's UCS(Ubiquitous Cloud Native Service) has adopted Karmada to support unified access and unified management of cross-cloud and cross-region clusters. By using Karmada, UCS realizes unified collaborative governance of cloud-native applications across clouds and regions, and 
  provides enterprises with a consistent global experience in cloud native business deployment, management, and application ecology.

The full adopter list can be found in our [website](https://karmada.io/docs/next/casestudies/adopters).

### Integration

In the past year, Karmada actively cooperates with other projects on the Kubernetes ecological chain to provide users with one-stop and high-value solutions.

The following are examples of ecosystem projects that have collaborated and integrated with Karmada:

* Karmada with [Istio](https://karmada.io/docs/userguide/service/working-with-istio-on-flat-network), the CNCF service mesh can implement multi-cluster traffic governance.
* Karmada with [Submariner](https://karmada.io/docs/userguide/network/working-with-submariner) can connect the network between multiple clusters across regions.
* Karmada with [Argo CD](https://karmada.io/docs/userguide/cicd/working-with-argocd) can manage workloads across clusters and simplify the delivery of multi-cloud applications.
* Karmada with [Flux](https://karmada.io/docs/userguide/cicd/working-with-flux) can support Helm chart propagation across cluster among multiple regions and multiple vendors.
* Karmada with [Gatekeeper(OPA)](https://karmada.io/docs/userguide/security-governance/working-with-gatekeeper) can unify management of security policies for multiple clusters.
* Karmada with [Kyverno](https://karmada.io/docs/userguide/security-governance/working-with-kyverno) can unify management of security policies for multiple clusters.
* Karmada with [Prometheus](https://karmada.io/docs/administrator/monitoring/working-with-prometheus) can build a multi-cloud unified monitoring view.
* Karmada with [Filebeat](https://karmada.io/docs/administrator/monitoring/working-with-filebeat) can implement unified log collection in multi-cloud scenarios.
* Karmada with [Velero](https://karmada.io/docs/administrator/backup/working-with-velero) can implement backup and restore of multi-cloud resource pools.

## Project goals

> How has the project performed against its goals since the last review?

Karmada aims to provide turnkey automation for multi-cluster application management in multi-cloud and hybrid cloud scenarios,
with key features such as centralized multi-cloud management, high availability, failure recovery, and traffic scheduling.

Karmada has been adhering to the following values since the inception of the project:

1. Provide a smooth evolution path for native Kubernetes, so that Karmada-based multi-cloud solutions can be seamlessly integrated into the cloud-native technology ecosystem, and provide enterprises with a smooth evolution solution from a single cluster to a multi-cloud architecture.
2. Provide high-availability scheduling, failover, multi-cluster service discovery, multi-cloud cluster lifecycle management and other capability sets in a modular manner and
   preset policy sets for a variety of typical user scenarios which allows users to freely customize the multi-cloud platform that suits them according to the actual situation of the enterprise.

Following the above goals, the biggest goals at that time were quite simply to:

* Build a extensible and open architecture and reach a stable core API and feature set that is reliable and mature
* Have production adopters that have successfully deployed Karmada into production environments

In the last year we released a total of 1 major version and 6 minor versions. As we released v1.0.0 version, the Karmada project has entered a stage of steady iteration.
Also, as CNCF's first multi-cloud container orchestration project, we solved many pain points of users using containers in multi-cloud scenarios and brought an excellent user experience to users.
We are glad to see more and more users have begun to seriously adopt Karmada and run it in production scenarios with great success.

For the past year's work, we summarize in the following points:

* **More powerful cross-cluster scheduling capabilities**. In the last year, we have done a lot of work on cross-cluster scheduling of applications. Facing a variety of user scenarios, we introduced richer scheduling strategies and introduced a new component named `karmada-scheduler-estimator` to improve scheduling accuracy. 
  What's more, we introduced `karmada-descheduler` to reschedule in case of cluster resource imbalance. Based on this, users can deliver their applications more easily among clusters across regions and vendors. 
* **Easier to manage the cluster and the resources on the cluster**. In the past year, we enhance the framework of the resource interpreter to enable users to customize the resource status collected to the control plane. We introduced the aggregated API to
  allow users to connect and operate member clusters from the control plane. We introduced a new component `karmada-search` to implement global search for multi-cluster resources. 
  Based on this, users no longer have to deal with tedious and repetitive configuration management, and no longer have to endure the management costs caused by fragmented API access portals.
* **High availability for multi-cloud applications**. In the past year, we support cross-cluster failover of applications.
  When a cluster fails, applications can smoothly migrate from the failed cluster to another available cluster. During the replicas migration process, Karmada can ensure that the service replicas does not drop to zero, thereby ensuring that the service will not be interrupted.
  Based on this, users can use Karmada to manage distributed applications with confidence.
* **More convenient user experience**. In the past year, we continue to optimize our command line tools. Now users can complete the creation of the karmada control plane and bootstrap token-based cluster registration with one click.
  Based on this, the learning cost of users using Karmada is further reduced and operators can use Karmada more freely.

> What are the current goals of the project? For example, are you working on major new features? Or are you concentrating on adoption or documentation?

The Karmada project continues to grow and has its sight on multiple goals for both the near term and long range:

* Enhance the security to relieve users' concerns about using in production environment. Security is always a concern of users in landing production. We will continue enhancing the security of the Karmada project and
  in-depth researching on the pain points of users in actual use.
* Improve the performance to adapt to larger scale landing scenarios. We have started an early effort around improving user experiences in large scale scenarios in the past releases. 
  We will continue to help our partners to solve intractable diseases in complex scenarios, so that our projects can create greater value for users.
* Integration of more existing Kubernetes tool chain to bring users a one-stop multi-cloud solution.
  The integration with the CNCF ecosystem has always been a major focus of our efforts.
  We believe that cooperation in different fields can better serve our users.
  We will continue to seek cooperation with other mature projects to form an open and prosperous ecosystem.
* Improve user experiences and simplify the getting started experience.
  Karmada has some innovative concepts that take a little while for new users to understand and internalize. 
  We want to invest in our documentation and getting started resources to streamline people's initial introduction to Karmada to the point where they are productive with it.
  We will continue to improve our documentation and cli tools to reduce the learning cost for users.
* Delivering high impact and high demand features.
  As CNCF's first multi-cloud project, we will continue to explore usage scenarios in the multi-cloud field, dedicate ourselves to solving users' difficulties and pain points, and provide high-quality new features.
  The planed new features are shown in [roadmap](https://github.com/karmada-io/karmada/blob/master/ROADMAP.md).

## How the CNCF Can Help

Similar to many other Sandbox projects, we wish to get the following help from CNCF:
- More channels to advocate the project.
- More chances to collaborate with other projects in CNCF or even out of CNCF.
- Technical writing support for project documents.

## Incubation

We are preparing for the incubation proposal.