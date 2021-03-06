
---
title: "Provider"
block_external_search_index: true
---



The provider type for the okta package. By default, resources use package-wide configuration
settings, however an explicit `Provider` instance may be created and passed during resource
construction to achieve fine-grained programmatic control over provider settings. See the
[documentation](https://www.pulumi.com/docs/reference/programming-model/#providers) for more information.

> This content is derived from https://github.com/articulate/terraform-provider-okta/blob/master/website/docs/index.html.markdown.



## Create a Provider Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/okta/#Provider">Provider</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/okta/#ProviderArgs">ProviderArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">Provider</span><span class="p">(resource_name, opts=None, </span>api_token=None<span class="p">, </span>backoff=None<span class="p">, </span>base_url=None<span class="p">, </span>max_retries=None<span class="p">, </span>max_wait_seconds=None<span class="p">, </span>min_wait_seconds=None<span class="p">, </span>org_name=None<span class="p">, </span>parallelism=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewProvider<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/?tab=doc#ProviderArgs">ProviderArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/?tab=doc#Provider">Provider</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Okta/Pulumi.Okta..Provider.html">Provider</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Okta/Pulumi.Pulumi.OktaArgs.html">ProviderArgs</a></span>? <span class="nx">args = null<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Api<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}API Token granting privileges to Okta API.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Backoff</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}Use exponential back off strategy for rate limits.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Base<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Okta url. (Use 'oktapreview.com' for Okta testing)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Retries</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}maximum number of retries to attempt before erroring out.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Wait<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}maximum seconds to wait when rate limit is hit. We use exponential backoffs when backoff is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Wait<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}minimum seconds to wait when rate limit is hit. We use exponential backoffs when backoff is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Org<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The organization to manage in Okta.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Parallelism</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Number of concurrent requests to make within a resource where bulk operations are not possible. Take note of
https://developer.okta.com/docs/api/getting_started/rate-limits.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Api<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}API Token granting privileges to Okta API.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Backoff</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}Use exponential back off strategy for rate limits.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Base<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The Okta url. (Use 'oktapreview.com' for Okta testing)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Retries</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}maximum number of retries to attempt before erroring out.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Wait<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}maximum seconds to wait when rate limit is hit. We use exponential backoffs when backoff is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Min<wbr>Wait<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}minimum seconds to wait when rate limit is hit. We use exponential backoffs when backoff is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Org<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The organization to manage in Okta.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Parallelism</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Number of concurrent requests to make within a resource where bulk operations are not possible. Take note of
https://developer.okta.com/docs/api/getting_started/rate-limits.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>api<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}API Token granting privileges to Okta API.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>backoff</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}Use exponential back off strategy for rate limits.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>base<wbr>Url</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The Okta url. (Use 'oktapreview.com' for Okta testing)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Retries</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}maximum number of retries to attempt before erroring out.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Wait<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}maximum seconds to wait when rate limit is hit. We use exponential backoffs when backoff is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min<wbr>Wait<wbr>Seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}minimum seconds to wait when rate limit is hit. We use exponential backoffs when backoff is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>org<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The organization to manage in Okta.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>parallelism</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Number of concurrent requests to make within a resource where bulk operations are not possible. Take note of
https://developer.okta.com/docs/api/getting_started/rate-limits.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>api_<wbr>token</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}API Token granting privileges to Okta API.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>backoff</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Use exponential back off strategy for rate limits.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>base_<wbr>url</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Okta url. (Use 'oktapreview.com' for Okta testing)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max_<wbr>retries</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}maximum number of retries to attempt before erroring out.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max_<wbr>wait_<wbr>seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}maximum seconds to wait when rate limit is hit. We use exponential backoffs when backoff is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>min_<wbr>wait_<wbr>seconds</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}minimum seconds to wait when rate limit is hit. We use exponential backoffs when backoff is enabled.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>org_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The organization to manage in Okta.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>parallelism</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Number of concurrent requests to make within a resource where bulk operations are not possible. Take note of
https://developer.okta.com/docs/api/getting_started/rate-limits.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}















<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-okta">https://github.com/pulumi/pulumi-okta</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>

