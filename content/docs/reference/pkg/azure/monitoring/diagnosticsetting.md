
---
title: "DiagnosticSetting"
block_external_search_index: true
---



Manages a Diagnostic Setting for an existing Resource.

## Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure from "@pulumi/azure";

const exampleResourceGroup = new azure.core.ResourceGroup("example", {
    location: "West Europe",
});
const exampleAccount = exampleResourceGroup.name.apply(name => azure.storage.getAccount({
    name: "examplestoracc",
    resourceGroupName: name,
}, { async: true }));
const exampleKeyVault = exampleResourceGroup.name.apply(name => azure.keyvault.getKeyVault({
    name: "example-vault",
    resourceGroupName: name,
}, { async: true }));
const exampleDiagnosticSetting = new azure.monitoring.DiagnosticSetting("example", {
    logs: [{
        category: "AuditEvent",
        enabled: false,
        retentionPolicy: {
            enabled: false,
        },
    }],
    metrics: [{
        category: "AllMetrics",
        retentionPolicy: {
            enabled: false,
        },
    }],
    storageAccountId: exampleAccount.id,
    targetResourceId: exampleKeyVault.id,
});
```

> This content is derived from https://github.com/terraform-providers/terraform-provider-azurerm/blob/master/website/docs/r/monitor_diagnostic_setting.html.markdown.



## Create a DiagnosticSetting Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azure/monitoring/#DiagnosticSetting">DiagnosticSetting</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azure/monitoring/#DiagnosticSettingArgs">DiagnosticSettingArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">DiagnosticSetting</span><span class="p">(resource_name, opts=None, </span>eventhub_authorization_rule_id=None<span class="p">, </span>eventhub_name=None<span class="p">, </span>log_analytics_destination_type=None<span class="p">, </span>log_analytics_workspace_id=None<span class="p">, </span>logs=None<span class="p">, </span>metrics=None<span class="p">, </span>name=None<span class="p">, </span>storage_account_id=None<span class="p">, </span>target_resource_id=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewDiagnosticSetting<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/monitoring?tab=doc#DiagnosticSettingArgs">DiagnosticSettingArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/monitoring?tab=doc#DiagnosticSetting">DiagnosticSetting</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Azure/Pulumi.Azure.Monitoring.DiagnosticSetting.html">DiagnosticSetting</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Azure/Pulumi.Azure.Monitoring.DiagnosticSettingArgs.html">DiagnosticSettingArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The arguments to use to populate this resource's properties.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The arguments to use to populate this resource's properties.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resource.</dd>
    <dt class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The arguments to use to populate this resource's properties.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

#### Resource Arguments




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Eventhub<wbr>Authorization<wbr>Rule<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of an Event Hub Namespace Authorization Rule used to send Diagnostics Data. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Eventhub<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Event Hub where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Log<wbr>Analytics<wbr>Destination<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}When set to 'Dedicated' logs sent to a Log Analytics workspace will go into resource specific tables, instead of the legacy AzureDiagnostics table.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Log<wbr>Analytics<wbr>Workspace<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of a Log Analytics Workspace where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Logs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettinglog">List&lt;Diagnostic<wbr>Setting<wbr>Log<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}One or more `log` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettingmetric">List&lt;Diagnostic<wbr>Setting<wbr>Metric<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}One or more `metric` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Diagnostic Setting. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Storage<wbr>Account<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}With this parameter you can specify a storage account which should be used to send the logs to. Parameter must be a valid Azure Resource ID. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Target<wbr>Resource<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of an existing Resource on which to configure Diagnostic Settings. Changing this forces a new resource to be created.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Eventhub<wbr>Authorization<wbr>Rule<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of an Event Hub Namespace Authorization Rule used to send Diagnostics Data. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Eventhub<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Event Hub where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Log<wbr>Analytics<wbr>Destination<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}When set to 'Dedicated' logs sent to a Log Analytics workspace will go into resource specific tables, instead of the legacy AzureDiagnostics table.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Log<wbr>Analytics<wbr>Workspace<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of a Log Analytics Workspace where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Logs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettinglog">[]Diagnostic<wbr>Setting<wbr>Log</a></span>
    </dt>
    <dd>{{% md %}}One or more `log` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettingmetric">[]Diagnostic<wbr>Setting<wbr>Metric</a></span>
    </dt>
    <dd>{{% md %}}One or more `metric` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Diagnostic Setting. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Storage<wbr>Account<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}With this parameter you can specify a storage account which should be used to send the logs to. Parameter must be a valid Azure Resource ID. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Target<wbr>Resource<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of an existing Resource on which to configure Diagnostic Settings. Changing this forces a new resource to be created.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>eventhub<wbr>Authorization<wbr>Rule<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of an Event Hub Namespace Authorization Rule used to send Diagnostics Data. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>eventhub<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Event Hub where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>log<wbr>Analytics<wbr>Destination<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}When set to 'Dedicated' logs sent to a Log Analytics workspace will go into resource specific tables, instead of the legacy AzureDiagnostics table.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>log<wbr>Analytics<wbr>Workspace<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of a Log Analytics Workspace where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>logs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettinglog">Diagnostic<wbr>Setting<wbr>Log[]?</a></span>
    </dt>
    <dd>{{% md %}}One or more `log` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettingmetric">Diagnostic<wbr>Setting<wbr>Metric[]?</a></span>
    </dt>
    <dd>{{% md %}}One or more `metric` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Diagnostic Setting. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>storage<wbr>Account<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}With this parameter you can specify a storage account which should be used to send the logs to. Parameter must be a valid Azure Resource ID. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>target<wbr>Resource<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of an existing Resource on which to configure Diagnostic Settings. Changing this forces a new resource to be created.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>eventhub_<wbr>authorization_<wbr>rule_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of an Event Hub Namespace Authorization Rule used to send Diagnostics Data. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>eventhub_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Event Hub where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>log_<wbr>analytics_<wbr>destination_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}When set to 'Dedicated' logs sent to a Log Analytics workspace will go into resource specific tables, instead of the legacy AzureDiagnostics table.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>log_<wbr>analytics_<wbr>workspace_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of a Log Analytics Workspace where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>logs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettinglog">List[Diagnostic<wbr>Setting<wbr>Log]</a></span>
    </dt>
    <dd>{{% md %}}One or more `log` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettingmetric">List[Diagnostic<wbr>Setting<wbr>Metric]</a></span>
    </dt>
    <dd>{{% md %}}One or more `metric` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Diagnostic Setting. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>storage_<wbr>account_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}With this parameter you can specify a storage account which should be used to send the logs to. Parameter must be a valid Azure Resource ID. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>target_<wbr>resource_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of an existing Resource on which to configure Diagnostic Settings. Changing this forces a new resource to be created.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## DiagnosticSetting Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Eventhub<wbr>Authorization<wbr>Rule<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of an Event Hub Namespace Authorization Rule used to send Diagnostics Data. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Eventhub<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Event Hub where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Log<wbr>Analytics<wbr>Destination<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}When set to 'Dedicated' logs sent to a Log Analytics workspace will go into resource specific tables, instead of the legacy AzureDiagnostics table.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Log<wbr>Analytics<wbr>Workspace<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of a Log Analytics Workspace where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Logs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettinglog">List&lt;Diagnostic<wbr>Setting<wbr>Log&gt;?</a></span>
    </dt>
    <dd>{{% md %}}One or more `log` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettingmetric">List&lt;Diagnostic<wbr>Setting<wbr>Metric&gt;?</a></span>
    </dt>
    <dd>{{% md %}}One or more `metric` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Diagnostic Setting. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Storage<wbr>Account<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}With this parameter you can specify a storage account which should be used to send the logs to. Parameter must be a valid Azure Resource ID. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Target<wbr>Resource<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of an existing Resource on which to configure Diagnostic Settings. Changing this forces a new resource to be created.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Eventhub<wbr>Authorization<wbr>Rule<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of an Event Hub Namespace Authorization Rule used to send Diagnostics Data. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Eventhub<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Event Hub where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Log<wbr>Analytics<wbr>Destination<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}When set to 'Dedicated' logs sent to a Log Analytics workspace will go into resource specific tables, instead of the legacy AzureDiagnostics table.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Log<wbr>Analytics<wbr>Workspace<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of a Log Analytics Workspace where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Logs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettinglog">[]Diagnostic<wbr>Setting<wbr>Log</a></span>
    </dt>
    <dd>{{% md %}}One or more `log` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettingmetric">[]Diagnostic<wbr>Setting<wbr>Metric</a></span>
    </dt>
    <dd>{{% md %}}One or more `metric` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Diagnostic Setting. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Storage<wbr>Account<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}With this parameter you can specify a storage account which should be used to send the logs to. Parameter must be a valid Azure Resource ID. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Target<wbr>Resource<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of an existing Resource on which to configure Diagnostic Settings. Changing this forces a new resource to be created.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>eventhub<wbr>Authorization<wbr>Rule<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of an Event Hub Namespace Authorization Rule used to send Diagnostics Data. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>eventhub<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Event Hub where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>log<wbr>Analytics<wbr>Destination<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}When set to 'Dedicated' logs sent to a Log Analytics workspace will go into resource specific tables, instead of the legacy AzureDiagnostics table.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>log<wbr>Analytics<wbr>Workspace<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of a Log Analytics Workspace where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>logs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettinglog">Diagnostic<wbr>Setting<wbr>Log[]?</a></span>
    </dt>
    <dd>{{% md %}}One or more `log` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettingmetric">Diagnostic<wbr>Setting<wbr>Metric[]?</a></span>
    </dt>
    <dd>{{% md %}}One or more `metric` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Diagnostic Setting. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>storage<wbr>Account<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}With this parameter you can specify a storage account which should be used to send the logs to. Parameter must be a valid Azure Resource ID. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>target<wbr>Resource<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of an existing Resource on which to configure Diagnostic Settings. Changing this forces a new resource to be created.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>eventhub_<wbr>authorization_<wbr>rule_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of an Event Hub Namespace Authorization Rule used to send Diagnostics Data. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>eventhub_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Event Hub where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>log_<wbr>analytics_<wbr>destination_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}When set to 'Dedicated' logs sent to a Log Analytics workspace will go into resource specific tables, instead of the legacy AzureDiagnostics table.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>log_<wbr>analytics_<wbr>workspace_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of a Log Analytics Workspace where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>logs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettinglog">List[Diagnostic<wbr>Setting<wbr>Log]</a></span>
    </dt>
    <dd>{{% md %}}One or more `log` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettingmetric">List[Diagnostic<wbr>Setting<wbr>Metric]</a></span>
    </dt>
    <dd>{{% md %}}One or more `metric` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Diagnostic Setting. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>storage_<wbr>account_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}With this parameter you can specify a storage account which should be used to send the logs to. Parameter must be a valid Azure Resource ID. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>target_<wbr>resource_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of an existing Resource on which to configure Diagnostic Settings. Changing this forces a new resource to be created.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing DiagnosticSetting Resource

Get an existing DiagnosticSetting resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azure/monitoring/#DiagnosticSettingState">DiagnosticSettingState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/azure/monitoring/#DiagnosticSetting">DiagnosticSetting</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>eventhub_authorization_rule_id=None<span class="p">, </span>eventhub_name=None<span class="p">, </span>log_analytics_destination_type=None<span class="p">, </span>log_analytics_workspace_id=None<span class="p">, </span>logs=None<span class="p">, </span>metrics=None<span class="p">, </span>name=None<span class="p">, </span>storage_account_id=None<span class="p">, </span>target_resource_id=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetDiagnosticSetting<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/monitoring?tab=doc#DiagnosticSettingState">DiagnosticSettingState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/monitoring?tab=doc#DiagnosticSetting">DiagnosticSetting</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Azure/Pulumi.Azure.Monitoring.DiagnosticSetting.html">DiagnosticSetting</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Azure/Pulumi.Azure.Monitoring.DiagnosticSettingState.html">DiagnosticSettingState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

The following state arguments are supported:



{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Eventhub<wbr>Authorization<wbr>Rule<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of an Event Hub Namespace Authorization Rule used to send Diagnostics Data. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Eventhub<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Event Hub where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Log<wbr>Analytics<wbr>Destination<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}When set to 'Dedicated' logs sent to a Log Analytics workspace will go into resource specific tables, instead of the legacy AzureDiagnostics table.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Log<wbr>Analytics<wbr>Workspace<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of a Log Analytics Workspace where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Logs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettinglog">List&lt;Diagnostic<wbr>Setting<wbr>Log<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}One or more `log` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettingmetric">List&lt;Diagnostic<wbr>Setting<wbr>Metric<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}One or more `metric` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Diagnostic Setting. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Storage<wbr>Account<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}With this parameter you can specify a storage account which should be used to send the logs to. Parameter must be a valid Azure Resource ID. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Resource<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of an existing Resource on which to configure Diagnostic Settings. Changing this forces a new resource to be created.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Eventhub<wbr>Authorization<wbr>Rule<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of an Event Hub Namespace Authorization Rule used to send Diagnostics Data. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Eventhub<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Event Hub where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Log<wbr>Analytics<wbr>Destination<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}When set to 'Dedicated' logs sent to a Log Analytics workspace will go into resource specific tables, instead of the legacy AzureDiagnostics table.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Log<wbr>Analytics<wbr>Workspace<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of a Log Analytics Workspace where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Logs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettinglog">[]Diagnostic<wbr>Setting<wbr>Log</a></span>
    </dt>
    <dd>{{% md %}}One or more `log` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettingmetric">[]Diagnostic<wbr>Setting<wbr>Metric</a></span>
    </dt>
    <dd>{{% md %}}One or more `metric` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Diagnostic Setting. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Storage<wbr>Account<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}With this parameter you can specify a storage account which should be used to send the logs to. Parameter must be a valid Azure Resource ID. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Resource<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of an existing Resource on which to configure Diagnostic Settings. Changing this forces a new resource to be created.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>eventhub<wbr>Authorization<wbr>Rule<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of an Event Hub Namespace Authorization Rule used to send Diagnostics Data. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>eventhub<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Event Hub where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>log<wbr>Analytics<wbr>Destination<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}When set to 'Dedicated' logs sent to a Log Analytics workspace will go into resource specific tables, instead of the legacy AzureDiagnostics table.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>log<wbr>Analytics<wbr>Workspace<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of a Log Analytics Workspace where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>logs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettinglog">Diagnostic<wbr>Setting<wbr>Log[]?</a></span>
    </dt>
    <dd>{{% md %}}One or more `log` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettingmetric">Diagnostic<wbr>Setting<wbr>Metric[]?</a></span>
    </dt>
    <dd>{{% md %}}One or more `metric` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Diagnostic Setting. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>storage<wbr>Account<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}With this parameter you can specify a storage account which should be used to send the logs to. Parameter must be a valid Azure Resource ID. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target<wbr>Resource<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of an existing Resource on which to configure Diagnostic Settings. Changing this forces a new resource to be created.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>eventhub_<wbr>authorization_<wbr>rule_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of an Event Hub Namespace Authorization Rule used to send Diagnostics Data. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>eventhub_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Event Hub where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>log_<wbr>analytics_<wbr>destination_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}When set to 'Dedicated' logs sent to a Log Analytics workspace will go into resource specific tables, instead of the legacy AzureDiagnostics table.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>log_<wbr>analytics_<wbr>workspace_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the ID of a Log Analytics Workspace where Diagnostics Data should be sent. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>logs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettinglog">List[Diagnostic<wbr>Setting<wbr>Log]</a></span>
    </dt>
    <dd>{{% md %}}One or more `log` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>metrics</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettingmetric">List[Diagnostic<wbr>Setting<wbr>Metric]</a></span>
    </dt>
    <dd>{{% md %}}One or more `metric` blocks as defined below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the Diagnostic Setting. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>storage_<wbr>account_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}With this parameter you can specify a storage account which should be used to send the logs to. Parameter must be a valid Azure Resource ID. Changing this forces a new resource to be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target_<wbr>resource_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of an existing Resource on which to configure Diagnostic Settings. Changing this forces a new resource to be created.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Diagnostic<wbr>Setting<wbr>Log</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#DiagnosticSettingLog">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#DiagnosticSettingLog">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/monitoring?tab=doc#DiagnosticSettingLogArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/monitoring?tab=doc#DiagnosticSettingLogOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Category</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a Diagnostic Log Category for this Resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Is this Diagnostic Log enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Retention<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettinglogretentionpolicy">Diagnostic<wbr>Setting<wbr>Log<wbr>Retention<wbr>Policy<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}A `retention_policy` block as defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Category</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a Diagnostic Log Category for this Resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Is this Diagnostic Log enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Retention<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettinglogretentionpolicy">Diagnostic<wbr>Setting<wbr>Log<wbr>Retention<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}A `retention_policy` block as defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>category</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a Diagnostic Log Category for this Resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Is this Diagnostic Log enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>retention<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettinglogretentionpolicy">Diagnostic<wbr>Setting<wbr>Log<wbr>Retention<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}A `retention_policy` block as defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>category</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of a Diagnostic Log Category for this Resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Is this Diagnostic Log enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>retention_<wbr>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettinglogretentionpolicy">Dict[Diagnostic<wbr>Setting<wbr>Log<wbr>Retention<wbr>Policy]</a></span>
    </dt>
    <dd>{{% md %}}A `retention_policy` block as defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Diagnostic<wbr>Setting<wbr>Log<wbr>Retention<wbr>Policy</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#DiagnosticSettingLogRetentionPolicy">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#DiagnosticSettingLogRetentionPolicy">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/monitoring?tab=doc#DiagnosticSettingLogRetentionPolicyArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/monitoring?tab=doc#DiagnosticSettingLogRetentionPolicyOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Days</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The number of days for which this Retention Policy should apply.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Is this Retention Policy enabled?
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Days</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The number of days for which this Retention Policy should apply.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Is this Retention Policy enabled?
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>days</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The number of days for which this Retention Policy should apply.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Is this Retention Policy enabled?
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>days</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The number of days for which this Retention Policy should apply.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Is this Retention Policy enabled?
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Diagnostic<wbr>Setting<wbr>Metric</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#DiagnosticSettingMetric">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#DiagnosticSettingMetric">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/monitoring?tab=doc#DiagnosticSettingMetricArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/monitoring?tab=doc#DiagnosticSettingMetricOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Category</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a Diagnostic Metric Category for this Resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Is this Diagnostic Metric enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Retention<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettingmetricretentionpolicy">Diagnostic<wbr>Setting<wbr>Metric<wbr>Retention<wbr>Policy<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}A `retention_policy` block as defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Category</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a Diagnostic Metric Category for this Resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Is this Diagnostic Metric enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Retention<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettingmetricretentionpolicy">Diagnostic<wbr>Setting<wbr>Metric<wbr>Retention<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}A `retention_policy` block as defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>category</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of a Diagnostic Metric Category for this Resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Is this Diagnostic Metric enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>retention<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettingmetricretentionpolicy">Diagnostic<wbr>Setting<wbr>Metric<wbr>Retention<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}A `retention_policy` block as defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>category</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of a Diagnostic Metric Category for this Resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Is this Diagnostic Metric enabled? Defaults to `true`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>retention_<wbr>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#diagnosticsettingmetricretentionpolicy">Dict[Diagnostic<wbr>Setting<wbr>Metric<wbr>Retention<wbr>Policy]</a></span>
    </dt>
    <dd>{{% md %}}A `retention_policy` block as defined below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Diagnostic<wbr>Setting<wbr>Metric<wbr>Retention<wbr>Policy</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/input/#DiagnosticSettingMetricRetentionPolicy">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/azure/types/output/#DiagnosticSettingMetricRetentionPolicy">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/monitoring?tab=doc#DiagnosticSettingMetricRetentionPolicyArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-azure/sdk/go/azure/monitoring?tab=doc#DiagnosticSettingMetricRetentionPolicyOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Days</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The number of days for which this Retention Policy should apply.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Is this Retention Policy enabled?
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Days</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The number of days for which this Retention Policy should apply.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Is this Retention Policy enabled?
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>days</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The number of days for which this Retention Policy should apply.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Is this Retention Policy enabled?
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>days</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The number of days for which this Retention Policy should apply.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Is this Retention Policy enabled?
{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure">https://github.com/pulumi/pulumi-azure</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>

