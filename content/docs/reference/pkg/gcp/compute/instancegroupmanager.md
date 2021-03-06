
---
title: "InstanceGroupManager"
block_external_search_index: true
---



The Google Compute Engine Instance Group Manager API creates and manages pools
of homogeneous Compute Engine virtual machine instances from a common instance
template. For more information, see [the official documentation](https://cloud.google.com/compute/docs/instance-groups/manager)
and [API](https://cloud.google.com/compute/docs/reference/latest/instanceGroupManagers)

> **Note:** Use [gcp.compute.RegionInstanceGroupManager](https://www.terraform.io/docs/providers/google/r/compute_region_instance_group_manager.html) to create a regional (multi-zone) instance group manager.

> This content is derived from https://github.com/terraform-providers/terraform-provider-google/blob/master/website/docs/r/compute_instance_group_manager.html.markdown.



## Create a InstanceGroupManager Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/gcp/compute/#InstanceGroupManager">InstanceGroupManager</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/gcp/compute/#InstanceGroupManagerArgs">InstanceGroupManagerArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">InstanceGroupManager</span><span class="p">(resource_name, opts=None, </span>auto_healing_policies=None<span class="p">, </span>base_instance_name=None<span class="p">, </span>description=None<span class="p">, </span>name=None<span class="p">, </span>named_ports=None<span class="p">, </span>project=None<span class="p">, </span>target_pools=None<span class="p">, </span>target_size=None<span class="p">, </span>update_policy=None<span class="p">, </span>versions=None<span class="p">, </span>wait_for_instances=None<span class="p">, </span>zone=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewInstanceGroupManager<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/go/gcp/compute?tab=doc#InstanceGroupManagerArgs">InstanceGroupManagerArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/go/gcp/compute?tab=doc#InstanceGroupManager">InstanceGroupManager</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Gcp/Pulumi.Gcp.Compute.InstanceGroupManager.html">InstanceGroupManager</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Gcp/Pulumi.Gcp.Compute.InstanceGroupManagerArgs.html">InstanceGroupManagerArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Auto<wbr>Healing<wbr>Policies</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerautohealingpolicies">Instance<wbr>Group<wbr>Manager<wbr>Auto<wbr>Healing<wbr>Policies<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The autohealing policies for this managed instance
group. You can specify only one value. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-managed-instances#monitoring_groups).
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Base<wbr>Instance<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The base instance name to use for
instances in this group. The value must be a valid
[RFC1035](https://www.ietf.org/rfc/rfc1035.txt) name. Supported characters
are lowercase letters, numbers, and hyphens (-). Instances are named by
appending a hyphen and a random four-character string to the base instance
name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An optional textual description of the instance
group manager.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Named<wbr>Ports</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagernamedport">List&lt;Instance<wbr>Group<wbr>Manager<wbr>Named<wbr>Port<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}The named port configuration. See the section below
for details on configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}The full URL of all target pools to which new
instances in the group are added. Updating the target pools attribute does
not affect existing instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}- The number of instances calculated as a fixed number or a percentage depending on the settings. Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Update<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerupdatepolicy">Instance<wbr>Group<wbr>Manager<wbr>Update<wbr>Policy<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The update policy for this managed instance group. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/updating-managed-instance-groups) and [API](https://cloud.google.com/compute/docs/reference/rest/beta/instanceGroupManagers/patch)
- - -
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Versions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerversion">List&lt;Instance<wbr>Group<wbr>Manager<wbr>Version<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Application versions managed by this instance group. Each
version deals with a specific instance template, allowing canary release scenarios.
Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Wait<wbr>For<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to wait for all instances to be created/updated before
returning. Note that if this is set to true and the operation does not succeed, this provider will
continue trying until it times out.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The zone that instances in this group should be created
in.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Auto<wbr>Healing<wbr>Policies</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerautohealingpolicies">*Instance<wbr>Group<wbr>Manager<wbr>Auto<wbr>Healing<wbr>Policies</a></span>
    </dt>
    <dd>{{% md %}}The autohealing policies for this managed instance
group. You can specify only one value. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-managed-instances#monitoring_groups).
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Base<wbr>Instance<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The base instance name to use for
instances in this group. The value must be a valid
[RFC1035](https://www.ietf.org/rfc/rfc1035.txt) name. Supported characters
are lowercase letters, numbers, and hyphens (-). Instances are named by
appending a hyphen and a random four-character string to the base instance
name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}An optional textual description of the instance
group manager.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Named<wbr>Ports</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagernamedport">[]Instance<wbr>Group<wbr>Manager<wbr>Named<wbr>Port</a></span>
    </dt>
    <dd>{{% md %}}The named port configuration. See the section below
for details on configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Project</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The full URL of all target pools to which new
instances in the group are added. Updating the target pools attribute does
not affect existing instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}- The number of instances calculated as a fixed number or a percentage depending on the settings. Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Update<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerupdatepolicy">*Instance<wbr>Group<wbr>Manager<wbr>Update<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}The update policy for this managed instance group. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/updating-managed-instance-groups) and [API](https://cloud.google.com/compute/docs/reference/rest/beta/instanceGroupManagers/patch)
- - -
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Versions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerversion">[]Instance<wbr>Group<wbr>Manager<wbr>Version</a></span>
    </dt>
    <dd>{{% md %}}Application versions managed by this instance group. Each
version deals with a specific instance template, allowing canary release scenarios.
Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Wait<wbr>For<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to wait for all instances to be created/updated before
returning. Note that if this is set to true and the operation does not succeed, this provider will
continue trying until it times out.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The zone that instances in this group should be created
in.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>auto<wbr>Healing<wbr>Policies</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerautohealingpolicies">Instance<wbr>Group<wbr>Manager<wbr>Auto<wbr>Healing<wbr>Policies?</a></span>
    </dt>
    <dd>{{% md %}}The autohealing policies for this managed instance
group. You can specify only one value. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-managed-instances#monitoring_groups).
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>base<wbr>Instance<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The base instance name to use for
instances in this group. The value must be a valid
[RFC1035](https://www.ietf.org/rfc/rfc1035.txt) name. Supported characters
are lowercase letters, numbers, and hyphens (-). Instances are named by
appending a hyphen and a random four-character string to the base instance
name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An optional textual description of the instance
group manager.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>named<wbr>Ports</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagernamedport">Instance<wbr>Group<wbr>Manager<wbr>Named<wbr>Port[]?</a></span>
    </dt>
    <dd>{{% md %}}The named port configuration. See the section below
for details on configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}The full URL of all target pools to which new
instances in the group are added. Updating the target pools attribute does
not affect existing instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}- The number of instances calculated as a fixed number or a percentage depending on the settings. Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>update<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerupdatepolicy">Instance<wbr>Group<wbr>Manager<wbr>Update<wbr>Policy?</a></span>
    </dt>
    <dd>{{% md %}}The update policy for this managed instance group. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/updating-managed-instance-groups) and [API](https://cloud.google.com/compute/docs/reference/rest/beta/instanceGroupManagers/patch)
- - -
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>versions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerversion">Instance<wbr>Group<wbr>Manager<wbr>Version[]</a></span>
    </dt>
    <dd>{{% md %}}Application versions managed by this instance group. Each
version deals with a specific instance template, allowing canary release scenarios.
Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>wait<wbr>For<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to wait for all instances to be created/updated before
returning. Note that if this is set to true and the operation does not succeed, this provider will
continue trying until it times out.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The zone that instances in this group should be created
in.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>auto_<wbr>healing_<wbr>policies</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerautohealingpolicies">Dict[Instance<wbr>Group<wbr>Manager<wbr>Auto<wbr>Healing<wbr>Policies]</a></span>
    </dt>
    <dd>{{% md %}}The autohealing policies for this managed instance
group. You can specify only one value. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-managed-instances#monitoring_groups).
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>base_<wbr>instance_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The base instance name to use for
instances in this group. The value must be a valid
[RFC1035](https://www.ietf.org/rfc/rfc1035.txt) name. Supported characters
are lowercase letters, numbers, and hyphens (-). Instances are named by
appending a hyphen and a random four-character string to the base instance
name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}An optional textual description of the instance
group manager.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>named_<wbr>ports</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagernamedport">List[Instance<wbr>Group<wbr>Manager<wbr>Named<wbr>Port]</a></span>
    </dt>
    <dd>{{% md %}}The named port configuration. See the section below
for details on configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>project</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target_<wbr>pools</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The full URL of all target pools to which new
instances in the group are added. Updating the target pools attribute does
not affect existing instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}- The number of instances calculated as a fixed number or a percentage depending on the settings. Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>update_<wbr>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerupdatepolicy">Dict[Instance<wbr>Group<wbr>Manager<wbr>Update<wbr>Policy]</a></span>
    </dt>
    <dd>{{% md %}}The update policy for this managed instance group. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/updating-managed-instance-groups) and [API](https://cloud.google.com/compute/docs/reference/rest/beta/instanceGroupManagers/patch)
- - -
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>versions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerversion">List[Instance<wbr>Group<wbr>Manager<wbr>Version]</a></span>
    </dt>
    <dd>{{% md %}}Application versions managed by this instance group. Each
version deals with a specific instance template, allowing canary release scenarios.
Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>wait_<wbr>for_<wbr>instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to wait for all instances to be created/updated before
returning. Note that if this is set to true and the operation does not succeed, this provider will
continue trying until it times out.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The zone that instances in this group should be created
in.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## InstanceGroupManager Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Auto<wbr>Healing<wbr>Policies</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerautohealingpolicies">Instance<wbr>Group<wbr>Manager<wbr>Auto<wbr>Healing<wbr>Policies?</a></span>
    </dt>
    <dd>{{% md %}}The autohealing policies for this managed instance
group. You can specify only one value. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-managed-instances#monitoring_groups).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Base<wbr>Instance<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The base instance name to use for
instances in this group. The value must be a valid
[RFC1035](https://www.ietf.org/rfc/rfc1035.txt) name. Supported characters
are lowercase letters, numbers, and hyphens (-). Instances are named by
appending a hyphen and a random four-character string to the base instance
name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An optional textual description of the instance
group manager.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Fingerprint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The fingerprint of the instance group manager.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Instance<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The full URL of the instance group created by the manager.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Named<wbr>Ports</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagernamedport">List&lt;Instance<wbr>Group<wbr>Manager<wbr>Named<wbr>Port&gt;?</a></span>
    </dt>
    <dd>{{% md %}}The named port configuration. See the section below
for details on configuration.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Self<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URL of the created resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Target<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}The full URL of all target pools to which new
instances in the group are added. Updating the target pools attribute does
not affect existing instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Target<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}- The number of instances calculated as a fixed number or a percentage depending on the settings. Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Update<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerupdatepolicy">Instance<wbr>Group<wbr>Manager<wbr>Update<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}The update policy for this managed instance group. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/updating-managed-instance-groups) and [API](https://cloud.google.com/compute/docs/reference/rest/beta/instanceGroupManagers/patch)
- - -
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Versions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerversion">List&lt;Instance<wbr>Group<wbr>Manager<wbr>Version&gt;</a></span>
    </dt>
    <dd>{{% md %}}Application versions managed by this instance group. Each
version deals with a specific instance template, allowing canary release scenarios.
Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Wait<wbr>For<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to wait for all instances to be created/updated before
returning. Note that if this is set to true and the operation does not succeed, this provider will
continue trying until it times out.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The zone that instances in this group should be created
in.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Auto<wbr>Healing<wbr>Policies</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerautohealingpolicies">*Instance<wbr>Group<wbr>Manager<wbr>Auto<wbr>Healing<wbr>Policies</a></span>
    </dt>
    <dd>{{% md %}}The autohealing policies for this managed instance
group. You can specify only one value. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-managed-instances#monitoring_groups).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Base<wbr>Instance<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The base instance name to use for
instances in this group. The value must be a valid
[RFC1035](https://www.ietf.org/rfc/rfc1035.txt) name. Supported characters
are lowercase letters, numbers, and hyphens (-). Instances are named by
appending a hyphen and a random four-character string to the base instance
name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}An optional textual description of the instance
group manager.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Fingerprint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The fingerprint of the instance group manager.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Instance<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The full URL of the instance group created by the manager.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Named<wbr>Ports</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagernamedport">[]Instance<wbr>Group<wbr>Manager<wbr>Named<wbr>Port</a></span>
    </dt>
    <dd>{{% md %}}The named port configuration. See the section below
for details on configuration.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Self<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URL of the created resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Target<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The full URL of all target pools to which new
instances in the group are added. Updating the target pools attribute does
not affect existing instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Target<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}- The number of instances calculated as a fixed number or a percentage depending on the settings. Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Update<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerupdatepolicy">Instance<wbr>Group<wbr>Manager<wbr>Update<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}The update policy for this managed instance group. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/updating-managed-instance-groups) and [API](https://cloud.google.com/compute/docs/reference/rest/beta/instanceGroupManagers/patch)
- - -
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Versions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerversion">[]Instance<wbr>Group<wbr>Manager<wbr>Version</a></span>
    </dt>
    <dd>{{% md %}}Application versions managed by this instance group. Each
version deals with a specific instance template, allowing canary release scenarios.
Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Wait<wbr>For<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to wait for all instances to be created/updated before
returning. Note that if this is set to true and the operation does not succeed, this provider will
continue trying until it times out.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The zone that instances in this group should be created
in.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>auto<wbr>Healing<wbr>Policies</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerautohealingpolicies">Instance<wbr>Group<wbr>Manager<wbr>Auto<wbr>Healing<wbr>Policies?</a></span>
    </dt>
    <dd>{{% md %}}The autohealing policies for this managed instance
group. You can specify only one value. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-managed-instances#monitoring_groups).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>base<wbr>Instance<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The base instance name to use for
instances in this group. The value must be a valid
[RFC1035](https://www.ietf.org/rfc/rfc1035.txt) name. Supported characters
are lowercase letters, numbers, and hyphens (-). Instances are named by
appending a hyphen and a random four-character string to the base instance
name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An optional textual description of the instance
group manager.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>fingerprint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The fingerprint of the instance group manager.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>instance<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The full URL of the instance group created by the manager.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>named<wbr>Ports</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagernamedport">Instance<wbr>Group<wbr>Manager<wbr>Named<wbr>Port[]?</a></span>
    </dt>
    <dd>{{% md %}}The named port configuration. See the section below
for details on configuration.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>self<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URL of the created resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>target<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}The full URL of all target pools to which new
instances in the group are added. Updating the target pools attribute does
not affect existing instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>target<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}- The number of instances calculated as a fixed number or a percentage depending on the settings. Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>update<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerupdatepolicy">Instance<wbr>Group<wbr>Manager<wbr>Update<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}The update policy for this managed instance group. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/updating-managed-instance-groups) and [API](https://cloud.google.com/compute/docs/reference/rest/beta/instanceGroupManagers/patch)
- - -
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>versions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerversion">Instance<wbr>Group<wbr>Manager<wbr>Version[]</a></span>
    </dt>
    <dd>{{% md %}}Application versions managed by this instance group. Each
version deals with a specific instance template, allowing canary release scenarios.
Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>wait<wbr>For<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to wait for all instances to be created/updated before
returning. Note that if this is set to true and the operation does not succeed, this provider will
continue trying until it times out.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The zone that instances in this group should be created
in.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>auto_<wbr>healing_<wbr>policies</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerautohealingpolicies">Dict[Instance<wbr>Group<wbr>Manager<wbr>Auto<wbr>Healing<wbr>Policies]</a></span>
    </dt>
    <dd>{{% md %}}The autohealing policies for this managed instance
group. You can specify only one value. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-managed-instances#monitoring_groups).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>base_<wbr>instance_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The base instance name to use for
instances in this group. The value must be a valid
[RFC1035](https://www.ietf.org/rfc/rfc1035.txt) name. Supported characters
are lowercase letters, numbers, and hyphens (-). Instances are named by
appending a hyphen and a random four-character string to the base instance
name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}An optional textual description of the instance
group manager.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>fingerprint</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The fingerprint of the instance group manager.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>instance_<wbr>group</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The full URL of the instance group created by the manager.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>named_<wbr>ports</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagernamedport">List[Instance<wbr>Group<wbr>Manager<wbr>Named<wbr>Port]</a></span>
    </dt>
    <dd>{{% md %}}The named port configuration. See the section below
for details on configuration.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>project</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>self_<wbr>link</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The URL of the created resource.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>target_<wbr>pools</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The full URL of all target pools to which new
instances in the group are added. Updating the target pools attribute does
not affect existing instances.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>target_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}- The number of instances calculated as a fixed number or a percentage depending on the settings. Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>update_<wbr>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerupdatepolicy">Dict[Instance<wbr>Group<wbr>Manager<wbr>Update<wbr>Policy]</a></span>
    </dt>
    <dd>{{% md %}}The update policy for this managed instance group. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/updating-managed-instance-groups) and [API](https://cloud.google.com/compute/docs/reference/rest/beta/instanceGroupManagers/patch)
- - -
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>versions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerversion">List[Instance<wbr>Group<wbr>Manager<wbr>Version]</a></span>
    </dt>
    <dd>{{% md %}}Application versions managed by this instance group. Each
version deals with a specific instance template, allowing canary release scenarios.
Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>wait_<wbr>for_<wbr>instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to wait for all instances to be created/updated before
returning. Note that if this is set to true and the operation does not succeed, this provider will
continue trying until it times out.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The zone that instances in this group should be created
in.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing InstanceGroupManager Resource

Get an existing InstanceGroupManager resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/gcp/compute/#InstanceGroupManagerState">InstanceGroupManagerState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/gcp/compute/#InstanceGroupManager">InstanceGroupManager</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>auto_healing_policies=None<span class="p">, </span>base_instance_name=None<span class="p">, </span>description=None<span class="p">, </span>fingerprint=None<span class="p">, </span>instance_group=None<span class="p">, </span>name=None<span class="p">, </span>named_ports=None<span class="p">, </span>project=None<span class="p">, </span>self_link=None<span class="p">, </span>target_pools=None<span class="p">, </span>target_size=None<span class="p">, </span>update_policy=None<span class="p">, </span>versions=None<span class="p">, </span>wait_for_instances=None<span class="p">, </span>zone=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetInstanceGroupManager<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/go/gcp/compute?tab=doc#InstanceGroupManagerState">InstanceGroupManagerState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/go/gcp/compute?tab=doc#InstanceGroupManager">InstanceGroupManager</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Gcp/Pulumi.Gcp.Compute.InstanceGroupManager.html">InstanceGroupManager</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Gcp/Pulumi.Gcp.Compute.InstanceGroupManagerState.html">InstanceGroupManagerState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Auto<wbr>Healing<wbr>Policies</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerautohealingpolicies">Instance<wbr>Group<wbr>Manager<wbr>Auto<wbr>Healing<wbr>Policies<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The autohealing policies for this managed instance
group. You can specify only one value. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-managed-instances#monitoring_groups).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Base<wbr>Instance<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The base instance name to use for
instances in this group. The value must be a valid
[RFC1035](https://www.ietf.org/rfc/rfc1035.txt) name. Supported characters
are lowercase letters, numbers, and hyphens (-). Instances are named by
appending a hyphen and a random four-character string to the base instance
name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An optional textual description of the instance
group manager.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fingerprint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The fingerprint of the instance group manager.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The full URL of the instance group created by the manager.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Named<wbr>Ports</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagernamedport">List&lt;Instance<wbr>Group<wbr>Manager<wbr>Named<wbr>Port<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}The named port configuration. See the section below
for details on configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Self<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The URL of the created resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}The full URL of all target pools to which new
instances in the group are added. Updating the target pools attribute does
not affect existing instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}- The number of instances calculated as a fixed number or a percentage depending on the settings. Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Update<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerupdatepolicy">Instance<wbr>Group<wbr>Manager<wbr>Update<wbr>Policy<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The update policy for this managed instance group. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/updating-managed-instance-groups) and [API](https://cloud.google.com/compute/docs/reference/rest/beta/instanceGroupManagers/patch)
- - -
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Versions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerversion">List&lt;Instance<wbr>Group<wbr>Manager<wbr>Version<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}Application versions managed by this instance group. Each
version deals with a specific instance template, allowing canary release scenarios.
Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Wait<wbr>For<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to wait for all instances to be created/updated before
returning. Note that if this is set to true and the operation does not succeed, this provider will
continue trying until it times out.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The zone that instances in this group should be created
in.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Auto<wbr>Healing<wbr>Policies</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerautohealingpolicies">*Instance<wbr>Group<wbr>Manager<wbr>Auto<wbr>Healing<wbr>Policies</a></span>
    </dt>
    <dd>{{% md %}}The autohealing policies for this managed instance
group. You can specify only one value. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-managed-instances#monitoring_groups).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Base<wbr>Instance<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The base instance name to use for
instances in this group. The value must be a valid
[RFC1035](https://www.ietf.org/rfc/rfc1035.txt) name. Supported characters
are lowercase letters, numbers, and hyphens (-). Instances are named by
appending a hyphen and a random four-character string to the base instance
name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}An optional textual description of the instance
group manager.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fingerprint</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The fingerprint of the instance group manager.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Instance<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The full URL of the instance group created by the manager.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Named<wbr>Ports</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagernamedport">[]Instance<wbr>Group<wbr>Manager<wbr>Named<wbr>Port</a></span>
    </dt>
    <dd>{{% md %}}The named port configuration. See the section below
for details on configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Project</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Self<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The URL of the created resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The full URL of all target pools to which new
instances in the group are added. Updating the target pools attribute does
not affect existing instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}- The number of instances calculated as a fixed number or a percentage depending on the settings. Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Update<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerupdatepolicy">*Instance<wbr>Group<wbr>Manager<wbr>Update<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}The update policy for this managed instance group. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/updating-managed-instance-groups) and [API](https://cloud.google.com/compute/docs/reference/rest/beta/instanceGroupManagers/patch)
- - -
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Versions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerversion">[]Instance<wbr>Group<wbr>Manager<wbr>Version</a></span>
    </dt>
    <dd>{{% md %}}Application versions managed by this instance group. Each
version deals with a specific instance template, allowing canary release scenarios.
Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Wait<wbr>For<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to wait for all instances to be created/updated before
returning. Note that if this is set to true and the operation does not succeed, this provider will
continue trying until it times out.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The zone that instances in this group should be created
in.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>auto<wbr>Healing<wbr>Policies</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerautohealingpolicies">Instance<wbr>Group<wbr>Manager<wbr>Auto<wbr>Healing<wbr>Policies?</a></span>
    </dt>
    <dd>{{% md %}}The autohealing policies for this managed instance
group. You can specify only one value. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-managed-instances#monitoring_groups).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>base<wbr>Instance<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The base instance name to use for
instances in this group. The value must be a valid
[RFC1035](https://www.ietf.org/rfc/rfc1035.txt) name. Supported characters
are lowercase letters, numbers, and hyphens (-). Instances are named by
appending a hyphen and a random four-character string to the base instance
name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}An optional textual description of the instance
group manager.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fingerprint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The fingerprint of the instance group manager.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>instance<wbr>Group</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The full URL of the instance group created by the manager.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>named<wbr>Ports</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagernamedport">Instance<wbr>Group<wbr>Manager<wbr>Named<wbr>Port[]?</a></span>
    </dt>
    <dd>{{% md %}}The named port configuration. See the section below
for details on configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>project</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>self<wbr>Link</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The URL of the created resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target<wbr>Pools</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}The full URL of all target pools to which new
instances in the group are added. Updating the target pools attribute does
not affect existing instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}- The number of instances calculated as a fixed number or a percentage depending on the settings. Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>update<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerupdatepolicy">Instance<wbr>Group<wbr>Manager<wbr>Update<wbr>Policy?</a></span>
    </dt>
    <dd>{{% md %}}The update policy for this managed instance group. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/updating-managed-instance-groups) and [API](https://cloud.google.com/compute/docs/reference/rest/beta/instanceGroupManagers/patch)
- - -
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>versions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerversion">Instance<wbr>Group<wbr>Manager<wbr>Version[]?</a></span>
    </dt>
    <dd>{{% md %}}Application versions managed by this instance group. Each
version deals with a specific instance template, allowing canary release scenarios.
Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>wait<wbr>For<wbr>Instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to wait for all instances to be created/updated before
returning. Note that if this is set to true and the operation does not succeed, this provider will
continue trying until it times out.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The zone that instances in this group should be created
in.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>auto_<wbr>healing_<wbr>policies</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerautohealingpolicies">Dict[Instance<wbr>Group<wbr>Manager<wbr>Auto<wbr>Healing<wbr>Policies]</a></span>
    </dt>
    <dd>{{% md %}}The autohealing policies for this managed instance
group. You can specify only one value. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-managed-instances#monitoring_groups).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>base_<wbr>instance_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The base instance name to use for
instances in this group. The value must be a valid
[RFC1035](https://www.ietf.org/rfc/rfc1035.txt) name. Supported characters
are lowercase letters, numbers, and hyphens (-). Instances are named by
appending a hyphen and a random four-character string to the base instance
name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}An optional textual description of the instance
group manager.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fingerprint</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The fingerprint of the instance group manager.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>instance_<wbr>group</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The full URL of the instance group created by the manager.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>named_<wbr>ports</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagernamedport">List[Instance<wbr>Group<wbr>Manager<wbr>Named<wbr>Port]</a></span>
    </dt>
    <dd>{{% md %}}The named port configuration. See the section below
for details on configuration.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>project</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>self_<wbr>link</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The URL of the created resource.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target_<wbr>pools</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The full URL of all target pools to which new
instances in the group are added. Updating the target pools attribute does
not affect existing instances.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}- The number of instances calculated as a fixed number or a percentage depending on the settings. Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>update_<wbr>policy</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerupdatepolicy">Dict[Instance<wbr>Group<wbr>Manager<wbr>Update<wbr>Policy]</a></span>
    </dt>
    <dd>{{% md %}}The update policy for this managed instance group. Structure is documented below. For more information, see the [official documentation](https://cloud.google.com/compute/docs/instance-groups/updating-managed-instance-groups) and [API](https://cloud.google.com/compute/docs/reference/rest/beta/instanceGroupManagers/patch)
- - -
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>versions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerversion">List[Instance<wbr>Group<wbr>Manager<wbr>Version]</a></span>
    </dt>
    <dd>{{% md %}}Application versions managed by this instance group. Each
version deals with a specific instance template, allowing canary release scenarios.
Structure is documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>wait_<wbr>for_<wbr>instances</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to wait for all instances to be created/updated before
returning. Note that if this is set to true and the operation does not succeed, this provider will
continue trying until it times out.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>zone</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The zone that instances in this group should be created
in.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Instance<wbr>Group<wbr>Manager<wbr>Auto<wbr>Healing<wbr>Policies</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/gcp/types/input/#InstanceGroupManagerAutoHealingPolicies">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/gcp/types/output/#InstanceGroupManagerAutoHealingPolicies">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/go/gcp/compute?tab=doc#InstanceGroupManagerAutoHealingPoliciesArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/go/gcp/compute?tab=doc#InstanceGroupManagerAutoHealingPoliciesOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Health<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The health check resource that signals autohealing.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Initial<wbr>Delay<wbr>Sec</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The number of seconds that the managed instance group waits before
it applies autohealing policies to new instances or recently recreated instances. Between 0 and 3600.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Health<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The health check resource that signals autohealing.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Initial<wbr>Delay<wbr>Sec</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The number of seconds that the managed instance group waits before
it applies autohealing policies to new instances or recently recreated instances. Between 0 and 3600.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>health<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The health check resource that signals autohealing.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>initial<wbr>Delay<wbr>Sec</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The number of seconds that the managed instance group waits before
it applies autohealing policies to new instances or recently recreated instances. Between 0 and 3600.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>health<wbr>Check</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The health check resource that signals autohealing.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>initial<wbr>Delay<wbr>Sec</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The number of seconds that the managed instance group waits before
it applies autohealing policies to new instances or recently recreated instances. Between 0 and 3600.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Instance<wbr>Group<wbr>Manager<wbr>Named<wbr>Port</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/gcp/types/input/#InstanceGroupManagerNamedPort">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/gcp/types/output/#InstanceGroupManagerNamedPort">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/go/gcp/compute?tab=doc#InstanceGroupManagerNamedPortArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/go/gcp/compute?tab=doc#InstanceGroupManagerNamedPortOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The port number.
- - -
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The port number.
- - -
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The port number.
- - -
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The port number.
- - -
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Instance<wbr>Group<wbr>Manager<wbr>Update<wbr>Policy</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/gcp/types/input/#InstanceGroupManagerUpdatePolicy">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/gcp/types/output/#InstanceGroupManagerUpdatePolicy">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/go/gcp/compute?tab=doc#InstanceGroupManagerUpdatePolicyArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/go/gcp/compute?tab=doc#InstanceGroupManagerUpdatePolicyOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Surge<wbr>Fixed</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}, The maximum number of instances that can be created above the specified targetSize during the update process. Conflicts with `max_surge_percent`. If neither is set, defaults to 1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Surge<wbr>Percent</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}, The maximum number of instances(calculated as percentage) that can be created above the specified targetSize during the update process. Conflicts with `max_surge_fixed`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Unavailable<wbr>Fixed</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}, The maximum number of instances that can be unavailable during the update process. Conflicts with `max_unavailable_percent`. If neither is set, defaults to 1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Unavailable<wbr>Percent</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}, The maximum number of instances(calculated as percentage) that can be unavailable during the update process. Conflicts with `max_unavailable_fixed`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Ready<wbr>Sec</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}, Minimum number of seconds to wait for after a newly created instance becomes available. This value must be from range [0, 3600]
- - -
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Minimal<wbr>Action</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}- Minimal action to be taken on an instance. You can specify either `RESTART` to restart existing instances or `REPLACE` to delete and create new instances from the target template. If you specify a `RESTART`, the Updater will attempt to perform that action only. However, if the Updater determines that the minimal action you specify is not enough to perform the update, it might perform a more disruptive action.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}- The type of update process. You can specify either `PROACTIVE` so that the instance group manager proactively executes actions in order to bring instances to their target versions or `OPPORTUNISTIC` so that no action is proactively executed but the update will be performed as part of other actions (for example, resizes or recreateInstances calls).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Surge<wbr>Fixed</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}, The maximum number of instances that can be created above the specified targetSize during the update process. Conflicts with `max_surge_percent`. If neither is set, defaults to 1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Surge<wbr>Percent</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}, The maximum number of instances(calculated as percentage) that can be created above the specified targetSize during the update process. Conflicts with `max_surge_fixed`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Unavailable<wbr>Fixed</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}, The maximum number of instances that can be unavailable during the update process. Conflicts with `max_unavailable_percent`. If neither is set, defaults to 1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Unavailable<wbr>Percent</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}, The maximum number of instances(calculated as percentage) that can be unavailable during the update process. Conflicts with `max_unavailable_fixed`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Ready<wbr>Sec</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}, Minimum number of seconds to wait for after a newly created instance becomes available. This value must be from range [0, 3600]
- - -
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Minimal<wbr>Action</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}- Minimal action to be taken on an instance. You can specify either `RESTART` to restart existing instances or `REPLACE` to delete and create new instances from the target template. If you specify a `RESTART`, the Updater will attempt to perform that action only. However, if the Updater determines that the minimal action you specify is not enough to perform the update, it might perform a more disruptive action.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}- The type of update process. You can specify either `PROACTIVE` so that the instance group manager proactively executes actions in order to bring instances to their target versions or `OPPORTUNISTIC` so that no action is proactively executed but the update will be performed as part of other actions (for example, resizes or recreateInstances calls).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Surge<wbr>Fixed</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}, The maximum number of instances that can be created above the specified targetSize during the update process. Conflicts with `max_surge_percent`. If neither is set, defaults to 1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Surge<wbr>Percent</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}, The maximum number of instances(calculated as percentage) that can be created above the specified targetSize during the update process. Conflicts with `max_surge_fixed`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Unavailable<wbr>Fixed</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}, The maximum number of instances that can be unavailable during the update process. Conflicts with `max_unavailable_percent`. If neither is set, defaults to 1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Unavailable<wbr>Percent</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}, The maximum number of instances(calculated as percentage) that can be unavailable during the update process. Conflicts with `max_unavailable_fixed`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min<wbr>Ready<wbr>Sec</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}, Minimum number of seconds to wait for after a newly created instance becomes available. This value must be from range [0, 3600]
- - -
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>minimal<wbr>Action</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}- Minimal action to be taken on an instance. You can specify either `RESTART` to restart existing instances or `REPLACE` to delete and create new instances from the target template. If you specify a `RESTART`, the Updater will attempt to perform that action only. However, if the Updater determines that the minimal action you specify is not enough to perform the update, it might perform a more disruptive action.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}- The type of update process. You can specify either `PROACTIVE` so that the instance group manager proactively executes actions in order to bring instances to their target versions or `OPPORTUNISTIC` so that no action is proactively executed but the update will be performed as part of other actions (for example, resizes or recreateInstances calls).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Surge<wbr>Fixed</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}, The maximum number of instances that can be created above the specified targetSize during the update process. Conflicts with `max_surge_percent`. If neither is set, defaults to 1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Surge<wbr>Percent</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}, The maximum number of instances(calculated as percentage) that can be created above the specified targetSize during the update process. Conflicts with `max_surge_fixed`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Unavailable<wbr>Fixed</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}, The maximum number of instances that can be unavailable during the update process. Conflicts with `max_unavailable_percent`. If neither is set, defaults to 1
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Unavailable<wbr>Percent</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}, The maximum number of instances(calculated as percentage) that can be unavailable during the update process. Conflicts with `max_unavailable_fixed`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min<wbr>Ready<wbr>Sec</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}, Minimum number of seconds to wait for after a newly created instance becomes available. This value must be from range [0, 3600]
- - -
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>minimal<wbr>Action</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}- Minimal action to be taken on an instance. You can specify either `RESTART` to restart existing instances or `REPLACE` to delete and create new instances from the target template. If you specify a `RESTART`, the Updater will attempt to perform that action only. However, if the Updater determines that the minimal action you specify is not enough to perform the update, it might perform a more disruptive action.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}- The type of update process. You can specify either `PROACTIVE` so that the instance group manager proactively executes actions in order to bring instances to their target versions or `OPPORTUNISTIC` so that no action is proactively executed but the update will be performed as part of other actions (for example, resizes or recreateInstances calls).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Instance<wbr>Group<wbr>Manager<wbr>Version</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/gcp/types/input/#InstanceGroupManagerVersion">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/gcp/types/output/#InstanceGroupManagerVersion">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/go/gcp/compute?tab=doc#InstanceGroupManagerVersionArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/go/gcp/compute?tab=doc#InstanceGroupManagerVersionOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Instance<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}- The full URL to an instance template from which all new instances of this version will be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerversiontargetsize">Instance<wbr>Group<wbr>Manager<wbr>Version<wbr>Target<wbr>Size<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}- The number of instances calculated as a fixed number or a percentage depending on the settings. Structure is documented below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Instance<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}- The full URL to an instance template from which all new instances of this version will be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerversiontargetsize">*Instance<wbr>Group<wbr>Manager<wbr>Version<wbr>Target<wbr>Size</a></span>
    </dt>
    <dd>{{% md %}}- The number of instances calculated as a fixed number or a percentage depending on the settings. Structure is documented below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>instance<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}- The full URL to an instance template from which all new instances of this version will be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target<wbr>Size</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerversiontargetsize">Instance<wbr>Group<wbr>Manager<wbr>Version<wbr>Target<wbr>Size?</a></span>
    </dt>
    <dd>{{% md %}}- The number of instances calculated as a fixed number or a percentage depending on the settings. Structure is documented below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>instance<wbr>Template</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}- The full URL to an instance template from which all new instances of this version will be created.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}- Version name.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target_<wbr>size</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instancegroupmanagerversiontargetsize">Dict[Instance<wbr>Group<wbr>Manager<wbr>Version<wbr>Target<wbr>Size]</a></span>
    </dt>
    <dd>{{% md %}}- The number of instances calculated as a fixed number or a percentage depending on the settings. Structure is documented below.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Instance<wbr>Group<wbr>Manager<wbr>Version<wbr>Target<wbr>Size</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/gcp/types/input/#InstanceGroupManagerVersionTargetSize">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/gcp/types/output/#InstanceGroupManagerVersionTargetSize">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/go/gcp/compute?tab=doc#InstanceGroupManagerVersionTargetSizeArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-gcp/sdk/go/gcp/compute?tab=doc#InstanceGroupManagerVersionTargetSizeOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Fixed</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}, The number of instances which are managed for this version. Conflicts with `percent`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Percent</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}, The number of instances (calculated as percentage) which are managed for this version. Conflicts with `fixed`.
Note that when using `percent`, rounding will be in favor of explicitly set `target_size` values; a managed instance group with 2 instances and 2 `version`s,
one of which has a `target_size.percent` of `60` will create 2 instances of that `version`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Fixed</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}, The number of instances which are managed for this version. Conflicts with `percent`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Percent</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}, The number of instances (calculated as percentage) which are managed for this version. Conflicts with `fixed`.
Note that when using `percent`, rounding will be in favor of explicitly set `target_size` values; a managed instance group with 2 instances and 2 `version`s,
one of which has a `target_size.percent` of `60` will create 2 instances of that `version`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>fixed</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}, The number of instances which are managed for this version. Conflicts with `percent`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>percent</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}, The number of instances (calculated as percentage) which are managed for this version. Conflicts with `fixed`.
Note that when using `percent`, rounding will be in favor of explicitly set `target_size` values; a managed instance group with 2 instances and 2 `version`s,
one of which has a `target_size.percent` of `60` will create 2 instances of that `version`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>fixed</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}, The number of instances which are managed for this version. Conflicts with `percent`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>percent</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}, The number of instances (calculated as percentage) which are managed for this version. Conflicts with `fixed`.
Note that when using `percent`, rounding will be in favor of explicitly set `target_size` values; a managed instance group with 2 instances and 2 `version`s,
one of which has a `target_size.percent` of `60` will create 2 instances of that `version`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-gcp">https://github.com/pulumi/pulumi-gcp</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>

