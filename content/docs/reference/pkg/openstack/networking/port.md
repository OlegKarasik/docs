
---
title: "Port"
block_external_search_index: true
---



Manages a V2 port resource within OpenStack.

## Example Usage

### Simple port

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as openstack from "@pulumi/openstack";

const network1 = new openstack.networking.Network("network_1", {
    adminStateUp: true,
});
const port1 = new openstack.networking.Port("port_1", {
    adminStateUp: true,
    networkId: network1.id,
});
```

### Port with physical binding information

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as openstack from "@pulumi/openstack";

const network1 = new openstack.networking.Network("network_1", {
    adminStateUp: true,
});
const port1 = new openstack.networking.Port("port_1", {
    adminStateUp: true,
    binding: {
        hostId: "b080b9cf-46e0-4ce8-ad47-0fd4accc872b",
        profile: `{
  "local_link_information": [
    {
      "switch_info": "info1",
      "port_id": "Ethernet3/4",
      "switch_id": "12:34:56:78:9A:BC"
    },
    {
      "switch_info": "info2",
      "port_id": "Ethernet3/4",
      "switch_id": "12:34:56:78:9A:BD"
    }
  ],
  "vlan_type": "allowed"
}
`,
        vnicType: "baremetal",
    },
    deviceId: "cdf70fcf-c161-4f24-9c70-96b3f5a54b71",
    deviceOwner: "baremetal:none",
    networkId: network1.id,
});
```

## Notes

### Ports and Instances

There are some notes to consider when connecting Instances to networks using
Ports. Please see the `openstack.compute.Instance` documentation for further
documentation.

> This content is derived from https://github.com/terraform-providers/terraform-provider-openstack/blob/master/website/docs/r/networking_port_v2.html.markdown.



## Create a Port Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/openstack/networking/#Port">Port</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/openstack/networking/#PortArgs">PortArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">Port</span><span class="p">(resource_name, opts=None, </span>admin_state_up=None<span class="p">, </span>allowed_address_pairs=None<span class="p">, </span>binding=None<span class="p">, </span>description=None<span class="p">, </span>device_id=None<span class="p">, </span>device_owner=None<span class="p">, </span>dns_name=None<span class="p">, </span>extra_dhcp_options=None<span class="p">, </span>fixed_ips=None<span class="p">, </span>mac_address=None<span class="p">, </span>name=None<span class="p">, </span>network_id=None<span class="p">, </span>no_fixed_ip=None<span class="p">, </span>no_security_groups=None<span class="p">, </span>port_security_enabled=None<span class="p">, </span>qos_policy_id=None<span class="p">, </span>region=None<span class="p">, </span>security_group_ids=None<span class="p">, </span>tags=None<span class="p">, </span>tenant_id=None<span class="p">, </span>value_specs=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewPort<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-openstack/sdk/go/openstack/networking?tab=doc#PortArgs">PortArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-openstack/sdk/go/openstack/networking?tab=doc#Port">Port</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Openstack/Pulumi.Openstack.Networking.Port.html">Port</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Openstack/Pulumi.Openstack.Networking.PortArgs.html">PortArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Admin<wbr>State<wbr>Up</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Administrative up/down status for the port
(must be "true" or "false" if provided). Changing this updates the
`admin_state_up` of an existing port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Allowed<wbr>Address<wbr>Pairs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portallowedaddresspair">List&lt;Port<wbr>Allowed<wbr>Address<wbr>Pair<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}An IP/MAC Address pair of additional IP
addresses that can be active on this port. The structure is described
below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Binding</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portbinding">Port<wbr>Binding<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The port binding allows to specify binding information
for the port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Human-readable description of the floating IP. Changing
this updates the `description` of an existing port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Device<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the device attached to the port. Changing this
creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Device<wbr>Owner</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The device owner of the Port. Changing this creates
a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Dns<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The port DNS name. Available, when Neutron DNS extension
is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Dhcp<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portextradhcpoption">List&lt;Port<wbr>Extra<wbr>Dhcp<wbr>Option<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}An extra DHCP option that needs to be configured
on the port. The structure is described below. Can be specified multiple
times.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fixed<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portfixedip">List&lt;Port<wbr>Fixed<wbr>Ip<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}An array of desired IPs for
this port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mac<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The additional MAC address.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of the DHCP option.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Network<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the network to attach the port to. Changing
this creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>No<wbr>Fixed<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Create a port with no fixed
IP address. This will also remove any fixed IPs previously set on a port. `true`
is the only valid value for this argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>No<wbr>Security<wbr>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}If set to
`true`, then no security groups are applied to the port. If set to `false` and
no `security_group_ids` are specified, then the Port will yield to the default
behavior of the Networking service, which is to usually apply the "default"
security group.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port<wbr>Security<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to explicitly enable or disable
port security on the port. Port Security is usually enabled by default, so
omitting argument will usually result in a value of "true". Setting this
explicitly to `false` will disable port security. In order to disable port
security, the port must not have any security groups. Valid values are `true`
and `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Qos<wbr>Policy<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Reference to the associated QoS policy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to create a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list
of security group IDs to apply to the port. The security groups must be
specified by ID and not name (as opposed to how they are configured with
the Compute Instance).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A set of string tags for the port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The owner of the Port. Required if admin wants
to create a port for another tenant. Changing this creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Value<wbr>Specs</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Map of additional options.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Admin<wbr>State<wbr>Up</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Administrative up/down status for the port
(must be "true" or "false" if provided). Changing this updates the
`admin_state_up` of an existing port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Allowed<wbr>Address<wbr>Pairs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portallowedaddresspair">[]Port<wbr>Allowed<wbr>Address<wbr>Pair</a></span>
    </dt>
    <dd>{{% md %}}An IP/MAC Address pair of additional IP
addresses that can be active on this port. The structure is described
below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Binding</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portbinding">*Port<wbr>Binding</a></span>
    </dt>
    <dd>{{% md %}}The port binding allows to specify binding information
for the port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Human-readable description of the floating IP. Changing
this updates the `description` of an existing port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Device<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the device attached to the port. Changing this
creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Device<wbr>Owner</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The device owner of the Port. Changing this creates
a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Dns<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The port DNS name. Available, when Neutron DNS extension
is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Dhcp<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portextradhcpoption">[]Port<wbr>Extra<wbr>Dhcp<wbr>Option</a></span>
    </dt>
    <dd>{{% md %}}An extra DHCP option that needs to be configured
on the port. The structure is described below. Can be specified multiple
times.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fixed<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portfixedip">[]Port<wbr>Fixed<wbr>Ip</a></span>
    </dt>
    <dd>{{% md %}}An array of desired IPs for
this port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mac<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The additional MAC address.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Name of the DHCP option.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Network<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the network to attach the port to. Changing
this creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>No<wbr>Fixed<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Create a port with no fixed
IP address. This will also remove any fixed IPs previously set on a port. `true`
is the only valid value for this argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>No<wbr>Security<wbr>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}If set to
`true`, then no security groups are applied to the port. If set to `false` and
no `security_group_ids` are specified, then the Port will yield to the default
behavior of the Networking service, which is to usually apply the "default"
security group.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port<wbr>Security<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to explicitly enable or disable
port security on the port. Port Security is usually enabled by default, so
omitting argument will usually result in a value of "true". Setting this
explicitly to `false` will disable port security. In order to disable port
security, the port must not have any security groups. Valid values are `true`
and `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Qos<wbr>Policy<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Reference to the associated QoS policy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to create a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list
of security group IDs to apply to the port. The security groups must be
specified by ID and not name (as opposed to how they are configured with
the Compute Instance).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A set of string tags for the port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The owner of the Port. Required if admin wants
to create a port for another tenant. Changing this creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Value<wbr>Specs</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Map of additional options.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>admin<wbr>State<wbr>Up</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Administrative up/down status for the port
(must be "true" or "false" if provided). Changing this updates the
`admin_state_up` of an existing port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>allowed<wbr>Address<wbr>Pairs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portallowedaddresspair">Port<wbr>Allowed<wbr>Address<wbr>Pair[]?</a></span>
    </dt>
    <dd>{{% md %}}An IP/MAC Address pair of additional IP
addresses that can be active on this port. The structure is described
below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>binding</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portbinding">Port<wbr>Binding?</a></span>
    </dt>
    <dd>{{% md %}}The port binding allows to specify binding information
for the port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Human-readable description of the floating IP. Changing
this updates the `description` of an existing port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>device<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the device attached to the port. Changing this
creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>device<wbr>Owner</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The device owner of the Port. Changing this creates
a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>dns<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The port DNS name. Available, when Neutron DNS extension
is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Dhcp<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portextradhcpoption">Port<wbr>Extra<wbr>Dhcp<wbr>Option[]?</a></span>
    </dt>
    <dd>{{% md %}}An extra DHCP option that needs to be configured
on the port. The structure is described below. Can be specified multiple
times.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fixed<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portfixedip">Port<wbr>Fixed<wbr>Ip[]?</a></span>
    </dt>
    <dd>{{% md %}}An array of desired IPs for
this port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mac<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The additional MAC address.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of the DHCP option.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>network<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the network to attach the port to. Changing
this creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>no<wbr>Fixed<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Create a port with no fixed
IP address. This will also remove any fixed IPs previously set on a port. `true`
is the only valid value for this argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>no<wbr>Security<wbr>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}If set to
`true`, then no security groups are applied to the port. If set to `false` and
no `security_group_ids` are specified, then the Port will yield to the default
behavior of the Networking service, which is to usually apply the "default"
security group.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port<wbr>Security<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to explicitly enable or disable
port security on the port. Port Security is usually enabled by default, so
omitting argument will usually result in a value of "true". Setting this
explicitly to `false` will disable port security. In order to disable port
security, the port must not have any security groups. Valid values are `true`
and `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>qos<wbr>Policy<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Reference to the associated QoS policy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to create a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list
of security group IDs to apply to the port. The security groups must be
specified by ID and not name (as opposed to how they are configured with
the Compute Instance).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A set of string tags for the port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The owner of the Port. Required if admin wants
to create a port for another tenant. Changing this creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>value<wbr>Specs</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Map of additional options.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>admin_<wbr>state_<wbr>up</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Administrative up/down status for the port
(must be "true" or "false" if provided). Changing this updates the
`admin_state_up` of an existing port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>allowed_<wbr>address_<wbr>pairs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portallowedaddresspair">List[Port<wbr>Allowed<wbr>Address<wbr>Pair]</a></span>
    </dt>
    <dd>{{% md %}}An IP/MAC Address pair of additional IP
addresses that can be active on this port. The structure is described
below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>binding</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portbinding">Dict[Port<wbr>Binding]</a></span>
    </dt>
    <dd>{{% md %}}The port binding allows to specify binding information
for the port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Human-readable description of the floating IP. Changing
this updates the `description` of an existing port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>device_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the device attached to the port. Changing this
creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>device_<wbr>owner</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The device owner of the Port. Changing this creates
a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>dns_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The port DNS name. Available, when Neutron DNS extension
is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra_<wbr>dhcp_<wbr>options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portextradhcpoption">List[Port<wbr>Extra<wbr>Dhcp<wbr>Option]</a></span>
    </dt>
    <dd>{{% md %}}An extra DHCP option that needs to be configured
on the port. The structure is described below. Can be specified multiple
times.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fixed_<wbr>ips</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portfixedip">List[Port<wbr>Fixed<wbr>Ip]</a></span>
    </dt>
    <dd>{{% md %}}An array of desired IPs for
this port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mac_<wbr>address</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The additional MAC address.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the DHCP option.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>network_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the network to attach the port to. Changing
this creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>no_<wbr>fixed_<wbr>ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Create a port with no fixed
IP address. This will also remove any fixed IPs previously set on a port. `true`
is the only valid value for this argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>no_<wbr>security_<wbr>groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to
`true`, then no security groups are applied to the port. If set to `false` and
no `security_group_ids` are specified, then the Port will yield to the default
behavior of the Networking service, which is to usually apply the "default"
security group.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port_<wbr>security_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to explicitly enable or disable
port security on the port. Port Security is usually enabled by default, so
omitting argument will usually result in a value of "true". Setting this
explicitly to `false` will disable port security. In order to disable port
security, the port must not have any security groups. Valid values are `true`
and `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>qos_<wbr>policy_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Reference to the associated QoS policy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to create a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>security_<wbr>group_<wbr>ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list
of security group IDs to apply to the port. The security groups must be
specified by ID and not name (as opposed to how they are configured with
the Compute Instance).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A set of string tags for the port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tenant_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The owner of the Port. Required if admin wants
to create a port for another tenant. Changing this creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>value_<wbr>specs</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Map of additional options.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## Port Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Admin<wbr>State<wbr>Up</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Administrative up/down status for the port
(must be "true" or "false" if provided). Changing this updates the
`admin_state_up` of an existing port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>All<wbr>Fixed<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}The collection of Fixed IP addresses on the port in the
order returned by the Network v2 API.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>All<wbr>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}The collection of Security Group IDs on the port
which have been explicitly and implicitly added.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>All<wbr>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}The collection of tags assigned on the port, which have been
explicitly and implicitly added.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Allowed<wbr>Address<wbr>Pairs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portallowedaddresspair">List&lt;Port<wbr>Allowed<wbr>Address<wbr>Pair&gt;?</a></span>
    </dt>
    <dd>{{% md %}}An IP/MAC Address pair of additional IP
addresses that can be active on this port. The structure is described
below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Binding</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portbinding">Port<wbr>Binding</a></span>
    </dt>
    <dd>{{% md %}}The port binding allows to specify binding information
for the port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Human-readable description of the floating IP. Changing
this updates the `description` of an existing port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Device<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the device attached to the port. Changing this
creates a new port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Device<wbr>Owner</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The device owner of the Port. Changing this creates
a new port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Dns<wbr>Assignments</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<ImmutableDictionary<string, object>></span>
    </dt>
    <dd>{{% md %}}The list of maps representing port DNS assignments.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Dns<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The port DNS name. Available, when Neutron DNS extension
is enabled.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Extra<wbr>Dhcp<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portextradhcpoption">List&lt;Port<wbr>Extra<wbr>Dhcp<wbr>Option&gt;?</a></span>
    </dt>
    <dd>{{% md %}}An extra DHCP option that needs to be configured
on the port. The structure is described below. Can be specified multiple
times.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Fixed<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portfixedip">List&lt;Port<wbr>Fixed<wbr>Ip&gt;?</a></span>
    </dt>
    <dd>{{% md %}}An array of desired IPs for
this port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Mac<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The additional MAC address.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the DHCP option.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Network<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the network to attach the port to. Changing
this creates a new port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>No<wbr>Fixed<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Create a port with no fixed
IP address. This will also remove any fixed IPs previously set on a port. `true`
is the only valid value for this argument.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>No<wbr>Security<wbr>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}If set to
`true`, then no security groups are applied to the port. If set to `false` and
no `security_group_ids` are specified, then the Port will yield to the default
behavior of the Networking service, which is to usually apply the "default"
security group.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Port<wbr>Security<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to explicitly enable or disable
port security on the port. Port Security is usually enabled by default, so
omitting argument will usually result in a value of "true". Setting this
explicitly to `false` will disable port security. In order to disable port
security, the port must not have any security groups. Valid values are `true`
and `false`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Qos<wbr>Policy<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Reference to the associated QoS policy.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to create a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list
of security group IDs to apply to the port. The security groups must be
specified by ID and not name (as opposed to how they are configured with
the Compute Instance).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A set of string tags for the port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The owner of the Port. Required if admin wants
to create a port for another tenant. Changing this creates a new port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Value<wbr>Specs</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Map of additional options.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Admin<wbr>State<wbr>Up</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Administrative up/down status for the port
(must be "true" or "false" if provided). Changing this updates the
`admin_state_up` of an existing port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>All<wbr>Fixed<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The collection of Fixed IP addresses on the port in the
order returned by the Network v2 API.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>All<wbr>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The collection of Security Group IDs on the port
which have been explicitly and implicitly added.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>All<wbr>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The collection of tags assigned on the port, which have been
explicitly and implicitly added.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Allowed<wbr>Address<wbr>Pairs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portallowedaddresspair">[]Port<wbr>Allowed<wbr>Address<wbr>Pair</a></span>
    </dt>
    <dd>{{% md %}}An IP/MAC Address pair of additional IP
addresses that can be active on this port. The structure is described
below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Binding</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portbinding">Port<wbr>Binding</a></span>
    </dt>
    <dd>{{% md %}}The port binding allows to specify binding information
for the port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Human-readable description of the floating IP. Changing
this updates the `description` of an existing port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Device<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the device attached to the port. Changing this
creates a new port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Device<wbr>Owner</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The device owner of the Port. Changing this creates
a new port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Dns<wbr>Assignments</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}The list of maps representing port DNS assignments.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Dns<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The port DNS name. Available, when Neutron DNS extension
is enabled.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Extra<wbr>Dhcp<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portextradhcpoption">[]Port<wbr>Extra<wbr>Dhcp<wbr>Option</a></span>
    </dt>
    <dd>{{% md %}}An extra DHCP option that needs to be configured
on the port. The structure is described below. Can be specified multiple
times.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Fixed<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portfixedip">[]Port<wbr>Fixed<wbr>Ip</a></span>
    </dt>
    <dd>{{% md %}}An array of desired IPs for
this port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Mac<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The additional MAC address.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the DHCP option.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Network<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the network to attach the port to. Changing
this creates a new port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>No<wbr>Fixed<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Create a port with no fixed
IP address. This will also remove any fixed IPs previously set on a port. `true`
is the only valid value for this argument.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>No<wbr>Security<wbr>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}If set to
`true`, then no security groups are applied to the port. If set to `false` and
no `security_group_ids` are specified, then the Port will yield to the default
behavior of the Networking service, which is to usually apply the "default"
security group.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Port<wbr>Security<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to explicitly enable or disable
port security on the port. Port Security is usually enabled by default, so
omitting argument will usually result in a value of "true". Setting this
explicitly to `false` will disable port security. In order to disable port
security, the port must not have any security groups. Valid values are `true`
and `false`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Qos<wbr>Policy<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Reference to the associated QoS policy.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to create a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list
of security group IDs to apply to the port. The security groups must be
specified by ID and not name (as opposed to how they are configured with
the Compute Instance).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A set of string tags for the port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The owner of the Port. Required if admin wants
to create a port for another tenant. Changing this creates a new port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Value<wbr>Specs</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Map of additional options.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>admin<wbr>State<wbr>Up</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Administrative up/down status for the port
(must be "true" or "false" if provided). Changing this updates the
`admin_state_up` of an existing port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>all<wbr>Fixed<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The collection of Fixed IP addresses on the port in the
order returned by the Network v2 API.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>all<wbr>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The collection of Security Group IDs on the port
which have been explicitly and implicitly added.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>all<wbr>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The collection of tags assigned on the port, which have been
explicitly and implicitly added.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>allowed<wbr>Address<wbr>Pairs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portallowedaddresspair">Port<wbr>Allowed<wbr>Address<wbr>Pair[]?</a></span>
    </dt>
    <dd>{{% md %}}An IP/MAC Address pair of additional IP
addresses that can be active on this port. The structure is described
below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>binding</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portbinding">Port<wbr>Binding</a></span>
    </dt>
    <dd>{{% md %}}The port binding allows to specify binding information
for the port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Human-readable description of the floating IP. Changing
this updates the `description` of an existing port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>device<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the device attached to the port. Changing this
creates a new port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>device<wbr>Owner</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The device owner of the Port. Changing this creates
a new port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>dns<wbr>Assignments</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}[]</span>
    </dt>
    <dd>{{% md %}}The list of maps representing port DNS assignments.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>dns<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The port DNS name. Available, when Neutron DNS extension
is enabled.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>extra<wbr>Dhcp<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portextradhcpoption">Port<wbr>Extra<wbr>Dhcp<wbr>Option[]?</a></span>
    </dt>
    <dd>{{% md %}}An extra DHCP option that needs to be configured
on the port. The structure is described below. Can be specified multiple
times.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>fixed<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portfixedip">Port<wbr>Fixed<wbr>Ip[]?</a></span>
    </dt>
    <dd>{{% md %}}An array of desired IPs for
this port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>mac<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The additional MAC address.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the DHCP option.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>network<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the network to attach the port to. Changing
this creates a new port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>no<wbr>Fixed<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Create a port with no fixed
IP address. This will also remove any fixed IPs previously set on a port. `true`
is the only valid value for this argument.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>no<wbr>Security<wbr>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}If set to
`true`, then no security groups are applied to the port. If set to `false` and
no `security_group_ids` are specified, then the Port will yield to the default
behavior of the Networking service, which is to usually apply the "default"
security group.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>port<wbr>Security<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Whether to explicitly enable or disable
port security on the port. Port Security is usually enabled by default, so
omitting argument will usually result in a value of "true". Setting this
explicitly to `false` will disable port security. In order to disable port
security, the port must not have any security groups. Valid values are `true`
and `false`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>qos<wbr>Policy<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Reference to the associated QoS policy.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to create a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list
of security group IDs to apply to the port. The security groups must be
specified by ID and not name (as opposed to how they are configured with
the Compute Instance).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A set of string tags for the port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The owner of the Port. Required if admin wants
to create a port for another tenant. Changing this creates a new port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>value<wbr>Specs</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Map of additional options.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>admin_<wbr>state_<wbr>up</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Administrative up/down status for the port
(must be "true" or "false" if provided). Changing this updates the
`admin_state_up` of an existing port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>all_<wbr>fixed_<wbr>ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The collection of Fixed IP addresses on the port in the
order returned by the Network v2 API.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>all_<wbr>security_<wbr>group_<wbr>ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The collection of Security Group IDs on the port
which have been explicitly and implicitly added.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>all_<wbr>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The collection of tags assigned on the port, which have been
explicitly and implicitly added.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>allowed_<wbr>address_<wbr>pairs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portallowedaddresspair">List[Port<wbr>Allowed<wbr>Address<wbr>Pair]</a></span>
    </dt>
    <dd>{{% md %}}An IP/MAC Address pair of additional IP
addresses that can be active on this port. The structure is described
below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>binding</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portbinding">Dict[Port<wbr>Binding]</a></span>
    </dt>
    <dd>{{% md %}}The port binding allows to specify binding information
for the port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Human-readable description of the floating IP. Changing
this updates the `description` of an existing port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>device_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the device attached to the port. Changing this
creates a new port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>device_<wbr>owner</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The device owner of the Port. Changing this creates
a new port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>dns_<wbr>assignments</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[Any>]</span>
    </dt>
    <dd>{{% md %}}The list of maps representing port DNS assignments.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>dns_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The port DNS name. Available, when Neutron DNS extension
is enabled.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>extra_<wbr>dhcp_<wbr>options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portextradhcpoption">List[Port<wbr>Extra<wbr>Dhcp<wbr>Option]</a></span>
    </dt>
    <dd>{{% md %}}An extra DHCP option that needs to be configured
on the port. The structure is described below. Can be specified multiple
times.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>fixed_<wbr>ips</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portfixedip">List[Port<wbr>Fixed<wbr>Ip]</a></span>
    </dt>
    <dd>{{% md %}}An array of desired IPs for
this port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>mac_<wbr>address</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The additional MAC address.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the DHCP option.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>network_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the network to attach the port to. Changing
this creates a new port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>no_<wbr>fixed_<wbr>ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Create a port with no fixed
IP address. This will also remove any fixed IPs previously set on a port. `true`
is the only valid value for this argument.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>no_<wbr>security_<wbr>groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to
`true`, then no security groups are applied to the port. If set to `false` and
no `security_group_ids` are specified, then the Port will yield to the default
behavior of the Networking service, which is to usually apply the "default"
security group.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>port_<wbr>security_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to explicitly enable or disable
port security on the port. Port Security is usually enabled by default, so
omitting argument will usually result in a value of "true". Setting this
explicitly to `false` will disable port security. In order to disable port
security, the port must not have any security groups. Valid values are `true`
and `false`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>qos_<wbr>policy_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Reference to the associated QoS policy.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to create a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>security_<wbr>group_<wbr>ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list
of security group IDs to apply to the port. The security groups must be
specified by ID and not name (as opposed to how they are configured with
the Compute Instance).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A set of string tags for the port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>tenant_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The owner of the Port. Required if admin wants
to create a port for another tenant. Changing this creates a new port.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>value_<wbr>specs</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Map of additional options.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing Port Resource

Get an existing Port resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/openstack/networking/#PortState">PortState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/openstack/networking/#Port">Port</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>admin_state_up=None<span class="p">, </span>all_fixed_ips=None<span class="p">, </span>all_security_group_ids=None<span class="p">, </span>all_tags=None<span class="p">, </span>allowed_address_pairs=None<span class="p">, </span>binding=None<span class="p">, </span>description=None<span class="p">, </span>device_id=None<span class="p">, </span>device_owner=None<span class="p">, </span>dns_assignments=None<span class="p">, </span>dns_name=None<span class="p">, </span>extra_dhcp_options=None<span class="p">, </span>fixed_ips=None<span class="p">, </span>mac_address=None<span class="p">, </span>name=None<span class="p">, </span>network_id=None<span class="p">, </span>no_fixed_ip=None<span class="p">, </span>no_security_groups=None<span class="p">, </span>port_security_enabled=None<span class="p">, </span>qos_policy_id=None<span class="p">, </span>region=None<span class="p">, </span>security_group_ids=None<span class="p">, </span>tags=None<span class="p">, </span>tenant_id=None<span class="p">, </span>value_specs=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetPort<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-openstack/sdk/go/openstack/networking?tab=doc#PortState">PortState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-openstack/sdk/go/openstack/networking?tab=doc#Port">Port</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Openstack/Pulumi.Openstack.Networking.Port.html">Port</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Openstack/Pulumi.Openstack.Networking.PortState.html">PortState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Admin<wbr>State<wbr>Up</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Administrative up/down status for the port
(must be "true" or "false" if provided). Changing this updates the
`admin_state_up` of an existing port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>All<wbr>Fixed<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}The collection of Fixed IP addresses on the port in the
order returned by the Network v2 API.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>All<wbr>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}The collection of Security Group IDs on the port
which have been explicitly and implicitly added.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>All<wbr>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}The collection of tags assigned on the port, which have been
explicitly and implicitly added.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Allowed<wbr>Address<wbr>Pairs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portallowedaddresspair">List&lt;Port<wbr>Allowed<wbr>Address<wbr>Pair<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}An IP/MAC Address pair of additional IP
addresses that can be active on this port. The structure is described
below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Binding</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portbinding">Port<wbr>Binding<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}The port binding allows to specify binding information
for the port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Human-readable description of the floating IP. Changing
this updates the `description` of an existing port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Device<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the device attached to the port. Changing this
creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Device<wbr>Owner</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The device owner of the Port. Changing this creates
a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Dns<wbr>Assignments</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<ImmutableDictionary<string, object>>?</span>
    </dt>
    <dd>{{% md %}}The list of maps representing port DNS assignments.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Dns<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The port DNS name. Available, when Neutron DNS extension
is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Dhcp<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portextradhcpoption">List&lt;Port<wbr>Extra<wbr>Dhcp<wbr>Option<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}An extra DHCP option that needs to be configured
on the port. The structure is described below. Can be specified multiple
times.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fixed<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portfixedip">List&lt;Port<wbr>Fixed<wbr>Ip<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}An array of desired IPs for
this port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mac<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The additional MAC address.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of the DHCP option.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Network<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the network to attach the port to. Changing
this creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>No<wbr>Fixed<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Create a port with no fixed
IP address. This will also remove any fixed IPs previously set on a port. `true`
is the only valid value for this argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>No<wbr>Security<wbr>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}If set to
`true`, then no security groups are applied to the port. If set to `false` and
no `security_group_ids` are specified, then the Port will yield to the default
behavior of the Networking service, which is to usually apply the "default"
security group.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port<wbr>Security<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Whether to explicitly enable or disable
port security on the port. Port Security is usually enabled by default, so
omitting argument will usually result in a value of "true". Setting this
explicitly to `false` will disable port security. In order to disable port
security, the port must not have any security groups. Valid values are `true`
and `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Qos<wbr>Policy<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Reference to the associated QoS policy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to create a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list
of security group IDs to apply to the port. The security groups must be
specified by ID and not name (as opposed to how they are configured with
the Compute Instance).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A set of string tags for the port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The owner of the Port. Required if admin wants
to create a port for another tenant. Changing this creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Value<wbr>Specs</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}Map of additional options.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Admin<wbr>State<wbr>Up</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Administrative up/down status for the port
(must be "true" or "false" if provided). Changing this updates the
`admin_state_up` of an existing port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>All<wbr>Fixed<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The collection of Fixed IP addresses on the port in the
order returned by the Network v2 API.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>All<wbr>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The collection of Security Group IDs on the port
which have been explicitly and implicitly added.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>All<wbr>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The collection of tags assigned on the port, which have been
explicitly and implicitly added.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Allowed<wbr>Address<wbr>Pairs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portallowedaddresspair">[]Port<wbr>Allowed<wbr>Address<wbr>Pair</a></span>
    </dt>
    <dd>{{% md %}}An IP/MAC Address pair of additional IP
addresses that can be active on this port. The structure is described
below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Binding</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portbinding">*Port<wbr>Binding</a></span>
    </dt>
    <dd>{{% md %}}The port binding allows to specify binding information
for the port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Human-readable description of the floating IP. Changing
this updates the `description` of an existing port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Device<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the device attached to the port. Changing this
creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Device<wbr>Owner</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The device owner of the Port. Changing this creates
a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Dns<wbr>Assignments</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}The list of maps representing port DNS assignments.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Dns<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The port DNS name. Available, when Neutron DNS extension
is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Extra<wbr>Dhcp<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portextradhcpoption">[]Port<wbr>Extra<wbr>Dhcp<wbr>Option</a></span>
    </dt>
    <dd>{{% md %}}An extra DHCP option that needs to be configured
on the port. The structure is described below. Can be specified multiple
times.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fixed<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portfixedip">[]Port<wbr>Fixed<wbr>Ip</a></span>
    </dt>
    <dd>{{% md %}}An array of desired IPs for
this port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mac<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The additional MAC address.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Name of the DHCP option.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Network<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the network to attach the port to. Changing
this creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>No<wbr>Fixed<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Create a port with no fixed
IP address. This will also remove any fixed IPs previously set on a port. `true`
is the only valid value for this argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>No<wbr>Security<wbr>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}If set to
`true`, then no security groups are applied to the port. If set to `false` and
no `security_group_ids` are specified, then the Port will yield to the default
behavior of the Networking service, which is to usually apply the "default"
security group.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port<wbr>Security<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Whether to explicitly enable or disable
port security on the port. Port Security is usually enabled by default, so
omitting argument will usually result in a value of "true". Setting this
explicitly to `false` will disable port security. In order to disable port
security, the port must not have any security groups. Valid values are `true`
and `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Qos<wbr>Policy<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Reference to the associated QoS policy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Region</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to create a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list
of security group IDs to apply to the port. The security groups must be
specified by ID and not name (as opposed to how they are configured with
the Compute Instance).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A set of string tags for the port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The owner of the Port. Required if admin wants
to create a port for another tenant. Changing this creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Value<wbr>Specs</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}Map of additional options.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>admin<wbr>State<wbr>Up</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Administrative up/down status for the port
(must be "true" or "false" if provided). Changing this updates the
`admin_state_up` of an existing port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>all<wbr>Fixed<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}The collection of Fixed IP addresses on the port in the
order returned by the Network v2 API.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>all<wbr>Security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}The collection of Security Group IDs on the port
which have been explicitly and implicitly added.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>all<wbr>Tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}The collection of tags assigned on the port, which have been
explicitly and implicitly added.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>allowed<wbr>Address<wbr>Pairs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portallowedaddresspair">Port<wbr>Allowed<wbr>Address<wbr>Pair[]?</a></span>
    </dt>
    <dd>{{% md %}}An IP/MAC Address pair of additional IP
addresses that can be active on this port. The structure is described
below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>binding</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portbinding">Port<wbr>Binding?</a></span>
    </dt>
    <dd>{{% md %}}The port binding allows to specify binding information
for the port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Human-readable description of the floating IP. Changing
this updates the `description` of an existing port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>device<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the device attached to the port. Changing this
creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>device<wbr>Owner</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The device owner of the Port. Changing this creates
a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>dns<wbr>Assignments</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}[]?</span>
    </dt>
    <dd>{{% md %}}The list of maps representing port DNS assignments.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>dns<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The port DNS name. Available, when Neutron DNS extension
is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra<wbr>Dhcp<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portextradhcpoption">Port<wbr>Extra<wbr>Dhcp<wbr>Option[]?</a></span>
    </dt>
    <dd>{{% md %}}An extra DHCP option that needs to be configured
on the port. The structure is described below. Can be specified multiple
times.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fixed<wbr>Ips</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portfixedip">Port<wbr>Fixed<wbr>Ip[]?</a></span>
    </dt>
    <dd>{{% md %}}An array of desired IPs for
this port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mac<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The additional MAC address.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Name of the DHCP option.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>network<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the network to attach the port to. Changing
this creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>no<wbr>Fixed<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Create a port with no fixed
IP address. This will also remove any fixed IPs previously set on a port. `true`
is the only valid value for this argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>no<wbr>Security<wbr>Groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}If set to
`true`, then no security groups are applied to the port. If set to `false` and
no `security_group_ids` are specified, then the Port will yield to the default
behavior of the Networking service, which is to usually apply the "default"
security group.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port<wbr>Security<wbr>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Whether to explicitly enable or disable
port security on the port. Port Security is usually enabled by default, so
omitting argument will usually result in a value of "true". Setting this
explicitly to `false` will disable port security. In order to disable port
security, the port must not have any security groups. Valid values are `true`
and `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>qos<wbr>Policy<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Reference to the associated QoS policy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to create a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>security<wbr>Group<wbr>Ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list
of security group IDs to apply to the port. The security groups must be
specified by ID and not name (as opposed to how they are configured with
the Compute Instance).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A set of string tags for the port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tenant<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The owner of the Port. Required if admin wants
to create a port for another tenant. Changing this creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>value<wbr>Specs</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}Map of additional options.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>admin_<wbr>state_<wbr>up</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Administrative up/down status for the port
(must be "true" or "false" if provided). Changing this updates the
`admin_state_up` of an existing port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>all_<wbr>fixed_<wbr>ips</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The collection of Fixed IP addresses on the port in the
order returned by the Network v2 API.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>all_<wbr>security_<wbr>group_<wbr>ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The collection of Security Group IDs on the port
which have been explicitly and implicitly added.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>all_<wbr>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}The collection of tags assigned on the port, which have been
explicitly and implicitly added.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>allowed_<wbr>address_<wbr>pairs</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portallowedaddresspair">List[Port<wbr>Allowed<wbr>Address<wbr>Pair]</a></span>
    </dt>
    <dd>{{% md %}}An IP/MAC Address pair of additional IP
addresses that can be active on this port. The structure is described
below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>binding</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portbinding">Dict[Port<wbr>Binding]</a></span>
    </dt>
    <dd>{{% md %}}The port binding allows to specify binding information
for the port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Human-readable description of the floating IP. Changing
this updates the `description` of an existing port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>device_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the device attached to the port. Changing this
creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>device_<wbr>owner</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The device owner of the Port. Changing this creates
a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>dns_<wbr>assignments</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[Any>]</span>
    </dt>
    <dd>{{% md %}}The list of maps representing port DNS assignments.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>dns_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The port DNS name. Available, when Neutron DNS extension
is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>extra_<wbr>dhcp_<wbr>options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portextradhcpoption">List[Port<wbr>Extra<wbr>Dhcp<wbr>Option]</a></span>
    </dt>
    <dd>{{% md %}}An extra DHCP option that needs to be configured
on the port. The structure is described below. Can be specified multiple
times.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fixed_<wbr>ips</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portfixedip">List[Port<wbr>Fixed<wbr>Ip]</a></span>
    </dt>
    <dd>{{% md %}}An array of desired IPs for
this port. The structure is described below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mac_<wbr>address</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The additional MAC address.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the DHCP option.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>network_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the network to attach the port to. Changing
this creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>no_<wbr>fixed_<wbr>ip</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Create a port with no fixed
IP address. This will also remove any fixed IPs previously set on a port. `true`
is the only valid value for this argument.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>no_<wbr>security_<wbr>groups</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If set to
`true`, then no security groups are applied to the port. If set to `false` and
no `security_group_ids` are specified, then the Port will yield to the default
behavior of the Networking service, which is to usually apply the "default"
security group.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port_<wbr>security_<wbr>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether to explicitly enable or disable
port security on the port. Port Security is usually enabled by default, so
omitting argument will usually result in a value of "true". Setting this
explicitly to `false` will disable port security. In order to disable port
security, the port must not have any security groups. Valid values are `true`
and `false`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>qos_<wbr>policy_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Reference to the associated QoS policy.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>region</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The region in which to obtain the V2 networking client.
A networking client is needed to create a port. If omitted, the
`region` argument of the provider is used. Changing this creates a new
port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>security_<wbr>group_<wbr>ids</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list
of security group IDs to apply to the port. The security groups must be
specified by ID and not name (as opposed to how they are configured with
the Compute Instance).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tags</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A set of string tags for the port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>tenant_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The owner of the Port. Required if admin wants
to create a port for another tenant. Changing this creates a new port.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>value_<wbr>specs</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}Map of additional options.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Port<wbr>Allowed<wbr>Address<wbr>Pair</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/openstack/types/input/#PortAllowedAddressPair">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/openstack/types/output/#PortAllowedAddressPair">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-openstack/sdk/go/openstack/networking?tab=doc#PortAllowedAddressPairArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-openstack/sdk/go/openstack/networking?tab=doc#PortAllowedAddressPairOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Ip<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The additional IP address.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mac<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The additional MAC address.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Ip<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The additional IP address.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Mac<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The additional MAC address.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>ip<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The additional IP address.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mac<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The additional MAC address.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>ip_<wbr>address</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The additional IP address.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>mac_<wbr>address</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The additional MAC address.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Port<wbr>Binding</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/openstack/types/input/#PortBinding">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/openstack/types/output/#PortBinding">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-openstack/sdk/go/openstack/networking?tab=doc#PortBindingArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-openstack/sdk/go/openstack/networking?tab=doc#PortBindingOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Host<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the host to allocate port on.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Profile</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Custom data to be passed as `binding:profile`. Data
must be passed as JSON.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vif<wbr>Details</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}A map of JSON strings containing additional
details for this specific binding.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vif<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The VNIC type of the port binding.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vnic<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}VNIC type for the port. Can either be `direct`,
`direct-physical`, `macvtap`, `normal`, `baremetal` or `virtio-forwarder`.
Default value is `normal`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Host<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ID of the host to allocate port on.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Profile</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Custom data to be passed as `binding:profile`. Data
must be passed as JSON.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vif<wbr>Details</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}A map of JSON strings containing additional
details for this specific binding.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vif<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The VNIC type of the port binding.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vnic<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}VNIC type for the port. Can either be `direct`,
`direct-physical`, `macvtap`, `normal`, `baremetal` or `virtio-forwarder`.
Default value is `normal`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>host<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ID of the host to allocate port on.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>profile</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Custom data to be passed as `binding:profile`. Data
must be passed as JSON.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vif<wbr>Details</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}A map of JSON strings containing additional
details for this specific binding.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vif<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The VNIC type of the port binding.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vnic<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}VNIC type for the port. Can either be `direct`,
`direct-physical`, `macvtap`, `normal`, `baremetal` or `virtio-forwarder`.
Default value is `normal`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>host<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the host to allocate port on.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>profile</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Custom data to be passed as `binding:profile`. Data
must be passed as JSON.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vif<wbr>Details</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}A map of JSON strings containing additional
details for this specific binding.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vif<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The VNIC type of the port binding.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vnic<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}VNIC type for the port. Can either be `direct`,
`direct-physical`, `macvtap`, `normal`, `baremetal` or `virtio-forwarder`.
Default value is `normal`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Port<wbr>Extra<wbr>Dhcp<wbr>Option</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/openstack/types/input/#PortExtraDhcpOption">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/openstack/types/output/#PortExtraDhcpOption">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-openstack/sdk/go/openstack/networking?tab=doc#PortExtraDhcpOptionArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-openstack/sdk/go/openstack/networking?tab=doc#PortExtraDhcpOptionOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Ip<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}IP protocol version. Defaults to 4.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the DHCP option.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Value of the DHCP option.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Ip<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}IP protocol version. Defaults to 4.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the DHCP option.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Value of the DHCP option.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>ip<wbr>Version</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}IP protocol version. Defaults to 4.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the DHCP option.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Value of the DHCP option.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>ip_<wbr>version</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}IP protocol version. Defaults to 4.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the DHCP option.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Value of the DHCP option.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Port<wbr>Fixed<wbr>Ip</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/openstack/types/input/#PortFixedIp">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/openstack/types/output/#PortFixedIp">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-openstack/sdk/go/openstack/networking?tab=doc#PortFixedIpArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-openstack/sdk/go/openstack/networking?tab=doc#PortFixedIpOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Ip<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The additional IP address.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Subnet<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Subnet in which to allocate IP address for
this port.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Ip<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The additional IP address.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Subnet<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Subnet in which to allocate IP address for
this port.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>ip<wbr>Address</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The additional IP address.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>subnet<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Subnet in which to allocate IP address for
this port.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>ip_<wbr>address</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The additional IP address.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>subnet_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Subnet in which to allocate IP address for
this port.
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

