[//]: # (title: TeamCity Cloud)
[//]: # (auxiliary-id: TeamCity Cloud)

<tip>

__TeamCity Cloud Public Beta is open!__

This page describes the current state of the TeamCity Cloud option, its Beta limitations, and target functionality. Please make sure to read it before joining our Public Beta program.

</tip>

## About TeamCity Cloud

TeamCity is a CI/CD server which key features are a powerful toolset and universality. With our Cloud version, we address the user demand in the most powerful CI/CD solution and make it available to you in a couple of minutes, with no need to maintain a server on-premise.

__If you are new to TeamCity__, the Cloud Beta is a great starting point as it automatically resolves the task of installing and configuring the server. After your [cloud TeamCity server is ready](#Starting+TeamCity+Cloud), you can proceed to our [_Configure and run your first build_](configure-and-run-your-first-build.md) guide.

When you register a TeamCity Cloud account, your own TeamCity server is automatically created in Amazon Web Services. The server operates on the newest version of TeamCity and currently provides Windows and Linux cloud agents out of the box.

We plan to officially release our Cloud version at the end of 2020. All users of the Beta program will receive an opportunity to migrate their TeamCity data to the released Cloud version.

## Starting TeamCity Cloud

To start TeamCity in cloud, __[create a Cloud Beta account](https://www.jetbrains.com/lp/teamcity/cloud-new/)__. In a matter of seconds, your server will be available under the `beta.teamcity.com` domain.

After the server is ready, an invitation link will be sent to your email. Proceed via this link to get to your administrative account. Everything is ready to build!

## TeamCity Cloud Maintenance

### TeamCity Cloud Server Administration

In case with TeamCity Cloud, the TeamCity team is responsible for handling all hardware and infrastructure maintenance of cloud servers. Because of that, the Cloud server has a limited administration functionality, comparing to the On-premise server.

The __Administration__ pages comprises the following sections:
* Under __Project-related Settings__, you can create projects and monitor server health and disk usage.
* Under __User Management__, you can add users, user groupes and roles, and assign permissions to users. Use the new _Invitations_ page to invite TeamCity users via email.
* Under __Server Administration__, you can import projects (for example, exported from your On-premise server), view usage statistics, and control general settings.

### Build Agents in Cloud

In TeamCity Cloud, you can either use self-hosted [build agents](build-agent.md) or request SaaS cloud agents.

<tip>

TeamCity Cloud supports agents hosted on Windows, Linux, and macOS. SaaS agents are available for Windows and Linux from the start, and macOS cloud agents will be introduced later in Beta.

</tip>
 

From the start, you get one Windows and two Linux images available in your default [pool](agent-pools.md). As soon as you run a build, TeamCity will automatically start an instance of the first suitable image. After the build is finished, the instance will be terminated by the idle timeout.

You can get extra agents by clicking __Install Build Agents__ in the upper right corner of the __Agents__ page. The number of available agents is limited by your license.   
We recommend using tokens to authenticate build agents on the TeamCity server. Click __Use authentication token__ and choose one of the two options: _Generate plain-text token_, or _Download config_ to create a ready-to-use [agent config file](build-agent-configuration.md).

In terms of Beta, cloud agents come with the following characteristics:

<table>

<tr>

<td>

Hardware

</td>

<td>

Software

</td>

</tr>

<tr>

<td>

* CPU:
* RAM:
* [TO DO]

</td>

<td>

* Java: Amazon Corretto 11
* Bundled plugins:
  * [TO DO]
* [TO DO]

</td>

</tr>


</table>


## Differences between TeamCity Cloud and On-premise

We plan to provide equal CI/CD experience to users of our Cloud and On-premise versions. However, the Cloud version is an automatically configured server and thus does not provide the same server settings as our On-premise solution.

Comparing to On-premise, TeamCity Cloud offers the following features:
* For improved security, you can generate authentication tokens for build agents in advance.
* Authorization via GitHub and Bitbucket is available. If you authenticate via any of these services, the respective [connection](integrating-teamcity-with-vcs-hosting-services.md#Configuring+Connections) will be preconfigured automatically.
* The __Administration | Invitations__ page allows automatically inviting users to the server. By default, you can add new users only via invitations. An invited user will be able to authenticate via GitHub or Bitbucket.

All the listed features will be introduced in our On-premise version in the nearest future.

TeamCity Cloud has the following limitations comparing to On-premise:
* Limited server configuration.
* No automatic [server diagnostics](teamcity-monitoring-and-diagnostics.md).
* No plugin management.
* Data is backed up and cleaned up automatically. The set of available configuration options may differ from the On-premise installations.
* Some settings are unavailable to Cloud admins: for example, cloud profile configuration or changing the location for storing external artifacts.

Some listed features might be implemented or receive their Cloud equivalents in terms of the Public Beta or first released versions of TeamCity Cloud.


## Troubleshooting and Feedback

To send your feedback or report issues, use our [YouTrack issue tracker](https://youtrack.jetbrains.com/issues/TW). You are welcome to discuss TeamCity Cloud in our [community forum](https://teamcity-support.jetbrains.com/hc/en-us/community/topics/).

Before inquiring, please refer to the F.A.Q. page on our website.

### Known Issues

[TO DO]