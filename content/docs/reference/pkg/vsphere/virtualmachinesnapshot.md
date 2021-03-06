
---
title: "VirtualMachineSnapshot"
block_external_search_index: true
---



The `vsphere..VirtualMachineSnapshot` resource can be used to manage snapshots
for a virtual machine.

For more information on managing snapshots and how they work in VMware, see
[here][ext-vm-snapshot-management].

[ext-vm-snapshot-management]: https://docs.vmware.com/en/VMware-vSphere/6.5/com.vmware.vsphere.vm_admin.doc/GUID-CA948C69-7F58-4519-AEB1-739545EA94E5.html

> **NOTE:** A snapshot in VMware differs from traditional disk snapshots, and
can contain the actual running state of the virtual machine, data for all disks
that have not been set to be independent from the snapshot (including ones that
have been attached via the [attach][docs-vsphere-virtual-machine-disk-attach]
parameter to the `vsphere..VirtualMachine` `disk` block), and even the
configuration of the virtual machine at the time of the snapshot. Virtual
machine, disk activity, and configuration changes post-snapshot are not
included in the original state. Use this resource with care! Neither VMware nor
HashiCorp recommends retaining snapshots for a extended period of time and does
NOT recommend using them as as backup feature. For more information on the
limitation of virtual machine snapshots, see [here][ext-vm-snap-limitations].

[docs-vsphere-virtual-machine-disk-attach]: /docs/providers/vsphere/r/virtual_machine.html#attach
[ext-vm-snap-limitations]: https://docs.vmware.com/en/VMware-vSphere/6.5/com.vmware.vsphere.vm_admin.doc/GUID-53F65726-A23B-4CF0-A7D5-48E584B88613.html

## Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as vsphere from "@pulumi/vsphere";

const demo1 = new vsphere.VirtualMachineSnapshot("demo1", {
    consolidate: true,
    description: "This is Demo Snapshot",
    memory: true,
    quiesce: true,
    removeChildren: false,
    snapshotName: "Snapshot Name",
    virtualMachineUuid: "9aac5551-a351-4158-8c5c-15a71e8ec5c9",
});
```

> This content is derived from https://github.com/terraform-providers/terraform-provider-vsphere/blob/master/website/docs/r/virtual_machine_snapshot.html.markdown.



## Create a VirtualMachineSnapshot Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/vsphere/#VirtualMachineSnapshot">VirtualMachineSnapshot</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/vsphere/#VirtualMachineSnapshotArgs">VirtualMachineSnapshotArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">VirtualMachineSnapshot</span><span class="p">(resource_name, opts=None, </span>consolidate=None<span class="p">, </span>description=None<span class="p">, </span>memory=None<span class="p">, </span>quiesce=None<span class="p">, </span>remove_children=None<span class="p">, </span>snapshot_name=None<span class="p">, </span>virtual_machine_uuid=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewVirtualMachineSnapshot<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-vsphere/sdk/go/vsphere/?tab=doc#VirtualMachineSnapshotArgs">VirtualMachineSnapshotArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-vsphere/sdk/go/vsphere/?tab=doc#VirtualMachineSnapshot">VirtualMachineSnapshot</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Vsphere/Pulumi.Vsphere..VirtualMachineSnapshot.html">VirtualMachineSnapshot</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Vsphere/Pulumi.Vsphere.VirtualMachineSnapshotArgs.html">VirtualMachineSnapshotArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Consolidate</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the delta disks involved in this
snapshot will be consolidated into the parent when this resource is
destroyed.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A description for the snapshot.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, a dump of the internal state of the
virtual machine is included in the snapshot.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Quiesce</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, and the virtual machine is powered
on when the snapshot is taken, VMware Tools is used to quiesce the file
system in the virtual machine.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Remove<wbr>Children</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the entire snapshot subtree
is removed when this resource is destroyed.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Snapshot<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the snapshot.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Virtual<wbr>Machine<wbr>Uuid</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The virtual machine UUID.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consolidate</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the delta disks involved in this
snapshot will be consolidated into the parent when this resource is
destroyed.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A description for the snapshot.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, a dump of the internal state of the
virtual machine is included in the snapshot.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Quiesce</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, and the virtual machine is powered
on when the snapshot is taken, VMware Tools is used to quiesce the file
system in the virtual machine.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Remove<wbr>Children</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the entire snapshot subtree
is removed when this resource is destroyed.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Snapshot<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the snapshot.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Virtual<wbr>Machine<wbr>Uuid</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The virtual machine UUID.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consolidate</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the delta disks involved in this
snapshot will be consolidated into the parent when this resource is
destroyed.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A description for the snapshot.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}If set to `true`, a dump of the internal state of the
virtual machine is included in the snapshot.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>quiesce</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}If set to `true`, and the virtual machine is powered
on when the snapshot is taken, VMware Tools is used to quiesce the file
system in the virtual machine.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>remove<wbr>Children</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the entire snapshot subtree
is removed when this resource is destroyed.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>snapshot<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the snapshot.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>virtual<wbr>Machine<wbr>Uuid</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The virtual machine UUID.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consolidate</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the delta disks involved in this
snapshot will be consolidated into the parent when this resource is
destroyed.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A description for the snapshot.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, a dump of the internal state of the
virtual machine is included in the snapshot.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>quiesce</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, and the virtual machine is powered
on when the snapshot is taken, VMware Tools is used to quiesce the file
system in the virtual machine.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>remove_<wbr>children</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the entire snapshot subtree
is removed when this resource is destroyed.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>snapshot_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the snapshot.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>virtual_<wbr>machine_<wbr>uuid</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The virtual machine UUID.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## VirtualMachineSnapshot Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Consolidate</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the delta disks involved in this
snapshot will be consolidated into the parent when this resource is
destroyed.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A description for the snapshot.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, a dump of the internal state of the
virtual machine is included in the snapshot.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Quiesce</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, and the virtual machine is powered
on when the snapshot is taken, VMware Tools is used to quiesce the file
system in the virtual machine.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Remove<wbr>Children</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the entire snapshot subtree
is removed when this resource is destroyed.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Snapshot<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the snapshot.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Virtual<wbr>Machine<wbr>Uuid</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The virtual machine UUID.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Consolidate</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the delta disks involved in this
snapshot will be consolidated into the parent when this resource is
destroyed.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A description for the snapshot.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, a dump of the internal state of the
virtual machine is included in the snapshot.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Quiesce</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, and the virtual machine is powered
on when the snapshot is taken, VMware Tools is used to quiesce the file
system in the virtual machine.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Remove<wbr>Children</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the entire snapshot subtree
is removed when this resource is destroyed.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Snapshot<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the snapshot.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Virtual<wbr>Machine<wbr>Uuid</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The virtual machine UUID.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>consolidate</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the delta disks involved in this
snapshot will be consolidated into the parent when this resource is
destroyed.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A description for the snapshot.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}If set to `true`, a dump of the internal state of the
virtual machine is included in the snapshot.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>quiesce</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}If set to `true`, and the virtual machine is powered
on when the snapshot is taken, VMware Tools is used to quiesce the file
system in the virtual machine.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>remove<wbr>Children</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the entire snapshot subtree
is removed when this resource is destroyed.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>snapshot<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the snapshot.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>virtual<wbr>Machine<wbr>Uuid</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The virtual machine UUID.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>consolidate</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the delta disks involved in this
snapshot will be consolidated into the parent when this resource is
destroyed.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A description for the snapshot.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, a dump of the internal state of the
virtual machine is included in the snapshot.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>quiesce</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, and the virtual machine is powered
on when the snapshot is taken, VMware Tools is used to quiesce the file
system in the virtual machine.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>remove_<wbr>children</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the entire snapshot subtree
is removed when this resource is destroyed.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>snapshot_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the snapshot.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>virtual_<wbr>machine_<wbr>uuid</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The virtual machine UUID.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing VirtualMachineSnapshot Resource

Get an existing VirtualMachineSnapshot resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/vsphere/#VirtualMachineSnapshotState">VirtualMachineSnapshotState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/vsphere/#VirtualMachineSnapshot">VirtualMachineSnapshot</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>consolidate=None<span class="p">, </span>description=None<span class="p">, </span>memory=None<span class="p">, </span>quiesce=None<span class="p">, </span>remove_children=None<span class="p">, </span>snapshot_name=None<span class="p">, </span>virtual_machine_uuid=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetVirtualMachineSnapshot<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-vsphere/sdk/go/vsphere/?tab=doc#VirtualMachineSnapshotState">VirtualMachineSnapshotState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-vsphere/sdk/go/vsphere/?tab=doc#VirtualMachineSnapshot">VirtualMachineSnapshot</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Vsphere/Pulumi.Vsphere..VirtualMachineSnapshot.html">VirtualMachineSnapshot</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Vsphere/Pulumi.Vsphere..VirtualMachineSnapshotState.html">VirtualMachineSnapshotState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Consolidate</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the delta disks involved in this
snapshot will be consolidated into the parent when this resource is
destroyed.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A description for the snapshot.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}If set to `true`, a dump of the internal state of the
virtual machine is included in the snapshot.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Quiesce</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}If set to `true`, and the virtual machine is powered
on when the snapshot is taken, VMware Tools is used to quiesce the file
system in the virtual machine.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Remove<wbr>Children</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the entire snapshot subtree
is removed when this resource is destroyed.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Snapshot<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the snapshot.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Virtual<wbr>Machine<wbr>Uuid</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The virtual machine UUID.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consolidate</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the delta disks involved in this
snapshot will be consolidated into the parent when this resource is
destroyed.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A description for the snapshot.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, a dump of the internal state of the
virtual machine is included in the snapshot.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Quiesce</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, and the virtual machine is powered
on when the snapshot is taken, VMware Tools is used to quiesce the file
system in the virtual machine.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Remove<wbr>Children</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the entire snapshot subtree
is removed when this resource is destroyed.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Snapshot<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the snapshot.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Virtual<wbr>Machine<wbr>Uuid</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The virtual machine UUID.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consolidate</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the delta disks involved in this
snapshot will be consolidated into the parent when this resource is
destroyed.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A description for the snapshot.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}If set to `true`, a dump of the internal state of the
virtual machine is included in the snapshot.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>quiesce</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}If set to `true`, and the virtual machine is powered
on when the snapshot is taken, VMware Tools is used to quiesce the file
system in the virtual machine.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>remove<wbr>Children</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the entire snapshot subtree
is removed when this resource is destroyed.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>snapshot<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the snapshot.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>virtual<wbr>Machine<wbr>Uuid</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The virtual machine UUID.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consolidate</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the delta disks involved in this
snapshot will be consolidated into the parent when this resource is
destroyed.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A description for the snapshot.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>memory</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, a dump of the internal state of the
virtual machine is included in the snapshot.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>quiesce</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, and the virtual machine is powered
on when the snapshot is taken, VMware Tools is used to quiesce the file
system in the virtual machine.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>remove_<wbr>children</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to `true`, the entire snapshot subtree
is removed when this resource is destroyed.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>snapshot_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the snapshot.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>virtual_<wbr>machine_<wbr>uuid</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The virtual machine UUID.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}











<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-vsphere">https://github.com/pulumi/pulumi-vsphere</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>

