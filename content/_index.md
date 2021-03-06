---
title: "BotKube"
---
<div class="mobiletitle">
<a href="/"><img src="/images/botkube-title.jpg"></a>
</div>
<div class="desktoptitle">
<a href="/"><img src="/images/botkube-title.jpg" width="486px" height="96px"></a>
</div>

<style>
.desktoptitle {
  float: center;
}

.mobiletitle {
  display: none;
}

.leftimage {
  width: 48%; float:left; display:inline-block;
}

.rightimage {
  width: 48%; float:right; display:inline-block;
}

.leftfeature {
  width: 48%; float:left; display:inline-block;
}

.centerfeature {
  width: 48%; float:center; display:inline-block;
}

.rightfeature {
  width: 48%; float:right; display:inline-block;
}

.visibledesktop {
  overflow: auto;
  display: block;
}

.visiblemobile {
  display: none;
}

@media screen and (max-width: 600px) {
  .desktoptitle {
    display: none;
  }
  .mobiletitle {
    display: block;
  }
  .leftimage {
    width: 100%;
  }
  .rightimage {
    width: 100%;
  }
  .leftfeature {
    width: 100%;
  }
  .rightfeature {
    width: 100%;
  }
  .visibledesktop {
    display: none;
  }
  .visiblemobile {
    overflow: auto;
    display: block;
  }
}
</style>

The BotKube Slack app helps you monitor your Kubernetes cluster, debug deployments and run specific checks on resources in the cluster.

<h2>What can BotKube do?</h2>
<div style="overflow: auto;">
  <div class="leftimage">
    <img src="/images/monitor.gif" style="border-radius:3%;">
  </div>
  <div class="rightimage">
    <h1>Monitor</h1>
    <ul>
      <li>BotKube watches Kubernetes resources and sends a notification to the Slack channel if any event occurs for example a ImagePullBackOff error.</li>
      <li>You can customize the objects and level of events you want to get from Kubernetes cluster.</li>
      <li>You can turn on/off notifications simply by sending a message to @BotKube</li>
    </ul>
  </div>
</div>

<div class="visiblemobile">
  <div class="leftimage">
    <img src="/images/exec.gif" style="border-radius:2%;">
  </div>
  <div class="rightimage" style="padding-top:10%;">
    <h1>Debug</h1>
    <ul>
    <li>Botkube can execute a kubectl commands on Kubernetes cluster without giving access to Kubeconfig or underlying infrastructure.</li>
    <li>With BotKube you can debug your deployment, services or anything about your cluster right from your Slack terminal ;) </li>
    </ul>
  </div>
</div>
<div class="visibledesktop">
  <div class="leftimage" style="padding-top:10%;">
    <h1>Debug</h1>
    <ul>
    <li>Botkube can execute a kubectl commands on Kubernetes cluster without giving access to Kubeconfig or underlying infrastructure.</li>
    <li>With BotKube you can debug your deployment, services or anything about your cluster right from your Slack terminal ;) </li>
    </ul>
  </div>
  <div class="rightimage">
    <img src="/images/exec.gif" style="border-radius:2%;">
  </div>
</div>

<div style="overflow: auto;">
  <div class="leftimage">
    <img src="/images/checks.gif" style="border-radius:2%;">
  </div>
  <div class="rightimage">
    <h1>Run Checks</h1>
    <ul>
    <li>Some checks are built in but you can define and add additional checks for specific resources or events.</li>
    <li>Filters allow you to more things for a specific event - such as adding a new message.</li>
    </ul>
  </div>
</div>

<center>
<h2>Features</h2>
<div style="overflow: auto;">
  <div class="leftfeature">
    <h4><i class="fas fa-fw fa-user-secret"></i> Privacy</h4> The backend for the Slack app runs in your Kubernetes cluster - thus you have complete control on your data and software.
  </div>
  <div class="rightfeature">
  <h4><i class="fas fa-terminal"></i> Execute kubectl commands</h4> Same old Kubectl syntax - just a new interface. You do not have to learn anything new!
  </div>
</div>

<div style="overflow: auto;">
  <div class="leftfeature">
    <h4><i class="fas fa-cogs"></i>  Debug Anywhere, Anytime</h4>
With @BotKube you can monitor and debug Kubernetes deployments from anywhere.
Even while you are camping without a laptop, you can use Slack mobile app and get crucial information.
  </div>
  <div class="rightfeature">
    <h4><i class="fas fa-cogs"></i>  Easy to configure</h4> Get notifications about things that you really care for. You can configure events or objects or namespaces that you want to be informed about.
  </div>
</div>

<div style="overflow: auto;">
  <div class="leftfeature">
    <h4><i class="fas fa-cloud"></i>  Deploy on any Kubernetes cluster</h4> You can deploy BotKube backend on any Kubernetes cluster, whether it is Minikube or cloud managed Kubernetes or anything in between.
  </div>
  <div class="rightfeature">
    <h4><i class="fas fa-plug"></i>  Add custom filters</h4> It is very easy to write your own filters and registering them to FilterEngine. Follow <a href=/filters>this</a> guide to know more.
  </div>
</div>

<div style="overflow: auto;">
  <div class="leftfeature">
    <h4><i class="fas fa-shield-alt"></i>  Security</h4> By default Botkube uses a READONLY service account, you can customize this to your needs.
  </div>
  <div class="rightfeature">
    <h4><i class="fab fa-github"></i>  Open source</h4> BotKube backend is open source and we welcome your requirements and contributions.
  </div>
</div>

<div style="overflow: auto;">
  <div class="centerfeature">
    <h4><i class="fas fa-tasks"></i>  Support for multiple interfaces</h4> Like Slack, BotKube can also be integrated with Mattermost and ElasticSearch. See <a href=/configuration>configuration</a> syntax for details.
  </div>
</div>

</center>
