
---
title: "QuoteSetV2"
block_external_search_index: true
---



Manages a V2 block storage quotaset resource within OpenStack.

> **Note:** This usually requires admin privileges.

> **Note:** This resource has a no-op deletion so no actual actions will be done against the OpenStack API 
    in case of delete call.

> This content is derived from https://github.com/terraform-providers/terraform-provider-openstack/blob/master/website/docs/r/blockstorage_quotaset_v2.html.markdown.



## Create a QuoteSetV2 Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/openstack/blockstorage/#QuoteSetV2">QuoteSetV2</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/openstack/blockstorage/#QuoteSetV2Args">QuoteSetV2Args</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">QuoteSetV2</span><span class="p">(resource_name, opts=None, </span>backup_gigabytes=None<span class="p">, </span>backups=None<span class="p">, </span>gigabytes=None<span class="p">, </span>groups=None<span class="p">, </span>per_volume_gigabytes=None<span class="p">, </span>project_id=None<span class="p">, </span>region=None<span class="p">, </span>snapshots=None<span class="p">, </span>volumes=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewQuoteSetV2<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-openstack/sdk/go/openstack/blockstorage?tab=doc#QuoteSetV2Args">QuoteSetV2Args</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-openstack/sdk/go/openstack/blockstorage?tab=doc#QuoteSetV2">QuoteSetV2</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Openstack/Pulumi.Openstack.Blockstorage.QuoteSetV2.html">QuoteSetV2</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Openstack/Pulumi.Openstack.BlockStorage.QuoteSetV2Args.html">QuoteSetV2Args</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Backup<wbr>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Quota value for backup gigabytes. Changing
this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Backups</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Quota value for backups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Quota value for groups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Per<wbr>Volume<wbr>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes per volume .
Changing this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the project to manage quotas. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The region in which to create the volume. If
omitted, the `region` argument of the provider is used. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Snapshots</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Quota value for snapshots. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Quota value for volumes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Backup<wbr>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Quota value for backup gigabytes. Changing
this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Backups</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Quota value for backups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Quota value for groups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Per<wbr>Volume<wbr>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes per volume .
Changing this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the project to manage quotas. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The region in which to create the volume. If
omitted, the `region` argument of the provider is used. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Snapshots</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Quota value for snapshots. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Quota value for volumes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>backup<wbr>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Quota value for backup gigabytes. Changing
this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>backups</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Quota value for backups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Quota value for groups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>per<wbr>Volume<wbr>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes per volume .
Changing this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the project to manage quotas. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The region in which to create the volume. If
omitted, the `region` argument of the provider is used. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>snapshots</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Quota value for snapshots. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Quota value for volumes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>backup_<wbr>gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for backup gigabytes. Changing
this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>backups</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for backups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for groups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>per_<wbr>volume_<wbr>gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes per volume .
Changing this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>project_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the project to manage quotas. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The region in which to create the volume. If
omitted, the `region` argument of the provider is used. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>snapshots</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for snapshots. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for volumes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## QuoteSetV2 Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Backup<wbr>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Quota value for backup gigabytes. Changing
this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Backups</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Quota value for backups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Quota value for groups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Per<wbr>Volume<wbr>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes per volume .
Changing this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the project to manage quotas. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region in which to create the volume. If
omitted, the `region` argument of the provider is used. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Snapshots</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Quota value for snapshots. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Quota value for volumes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Backup<wbr>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Quota value for backup gigabytes. Changing
this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Backups</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Quota value for backups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Quota value for groups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Per<wbr>Volume<wbr>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes per volume .
Changing this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the project to manage quotas. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region in which to create the volume. If
omitted, the `region` argument of the provider is used. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Snapshots</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Quota value for snapshots. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Quota value for volumes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>backup<wbr>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Quota value for backup gigabytes. Changing
this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>backups</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Quota value for backups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Quota value for groups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>per<wbr>Volume<wbr>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes per volume .
Changing this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the project to manage quotas. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region in which to create the volume. If
omitted, the `region` argument of the provider is used. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>snapshots</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Quota value for snapshots. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Quota value for volumes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>backup_<wbr>gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for backup gigabytes. Changing
this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>backups</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for backups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for groups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>per_<wbr>volume_<wbr>gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes per volume .
Changing this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>project_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the project to manage quotas. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The region in which to create the volume. If
omitted, the `region` argument of the provider is used. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>snapshots</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for snapshots. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for volumes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing QuoteSetV2 Resource

Get an existing QuoteSetV2 resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/openstack/blockstorage/#QuoteSetV2State">QuoteSetV2State</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/openstack/blockstorage/#QuoteSetV2">QuoteSetV2</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>backup_gigabytes=None<span class="p">, </span>backups=None<span class="p">, </span>gigabytes=None<span class="p">, </span>groups=None<span class="p">, </span>per_volume_gigabytes=None<span class="p">, </span>project_id=None<span class="p">, </span>region=None<span class="p">, </span>snapshots=None<span class="p">, </span>volumes=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetQuoteSetV2<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-openstack/sdk/go/openstack/blockstorage?tab=doc#QuoteSetV2State">QuoteSetV2State</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-openstack/sdk/go/openstack/blockstorage?tab=doc#QuoteSetV2">QuoteSetV2</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Openstack/Pulumi.Openstack.Blockstorage.QuoteSetV2.html">QuoteSetV2</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Openstack/Pulumi.Openstack.Blockstorage.QuoteSetV2State.html">QuoteSetV2State</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Backup<wbr>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Quota value for backup gigabytes. Changing
this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Backups</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Quota value for backups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Quota value for groups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Per<wbr>Volume<wbr>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes per volume .
Changing this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}ID of the project to manage quotas. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The region in which to create the volume. If
omitted, the `region` argument of the provider is used. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Snapshots</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Quota value for snapshots. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Quota value for volumes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Backup<wbr>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Quota value for backup gigabytes. Changing
this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Backups</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Quota value for backups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Quota value for groups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Per<wbr>Volume<wbr>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes per volume .
Changing this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}ID of the project to manage quotas. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The region in which to create the volume. If
omitted, the `region` argument of the provider is used. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Snapshots</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Quota value for snapshots. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Quota value for volumes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>backup<wbr>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Quota value for backup gigabytes. Changing
this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>backups</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Quota value for backups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Quota value for groups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>per<wbr>Volume<wbr>Gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes per volume .
Changing this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>project<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}ID of the project to manage quotas. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The region in which to create the volume. If
omitted, the `region` argument of the provider is used. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>snapshots</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Quota value for snapshots. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Quota value for volumes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>backup_<wbr>gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for backup gigabytes. Changing
this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>backups</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for backups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for groups. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>per_<wbr>volume_<wbr>gigabytes</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for gigabytes per volume .
Changing this updates the existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>project_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the project to manage quotas. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The region in which to create the volume. If
omitted, the `region` argument of the provider is used. Changing this
creates a new quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>snapshots</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for snapshots. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>volumes</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Quota value for volumes. Changing this updates the
existing quotaset.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}











<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-openstack">https://github.com/pulumi/pulumi-openstack</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>

