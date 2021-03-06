
---
title: "ListenerRule"
block_external_search_index: true
---



Provides a Load Balancer Listener Rule resource.

> **Note:** `aws.alb.ListenerRule` is known as `aws.lb.ListenerRule`. The functionality is identical.

{{% examples %}}
## Example Usage
{{% example %}}

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const frontEndLoadBalancer = new aws.lb.LoadBalancer("front_end", {});
const frontEndListener = new aws.lb.Listener("front_end", {});
const static = new aws.lb.ListenerRule("static", {
    actions: [{
        targetGroupArn: aws_lb_target_group_static.arn,
        type: "forward",
    }],
    conditions: [
        {
            pathPattern: {
                values: ["/static/*"],
            },
        },
        {
            hostHeader: {
                values: ["example.com"],
            },
        },
    ],
    listenerArn: frontEndListener.arn,
    priority: 100,
});
const hostBasedRouting = new aws.lb.ListenerRule("host_based_routing", {
    actions: [{
        targetGroupArn: aws_lb_target_group_static.arn,
        type: "forward",
    }],
    conditions: [{
        hostHeader: {
            values: ["my-service.*.mydomain.io"],
        },
    }],
    listenerArn: frontEndListener.arn,
    priority: 99,
});
const redirectHttpToHttps = new aws.lb.ListenerRule("redirect_http_to_https", {
    actions: [{
        redirect: {
            port: "443",
            protocol: "HTTPS",
            statusCode: "HTTP_301",
        },
        type: "redirect",
    }],
    conditions: [{
        httpHeader: {
            httpHeaderName: "X-Forwarded-For",
            values: ["192.168.1.*"],
        },
    }],
    listenerArn: frontEndListener.arn,
});
const healthCheck = new aws.lb.ListenerRule("health_check", {
    actions: [{
        fixedResponse: {
            contentType: "text/plain",
            messageBody: "HEALTHY",
            statusCode: "200",
        },
        type: "fixed-response",
    }],
    conditions: [{
        queryStrings: [
            {
                key: "health",
                value: "check",
            },
            {
                value: "bar",
            },
        ],
    }],
    listenerArn: frontEndListener.arn,
});
const pool = new aws.cognito.UserPool("pool", {});
const client = new aws.cognito.UserPoolClient("client", {});
const domain = new aws.cognito.UserPoolDomain("domain", {});
const admin = new aws.lb.ListenerRule("admin", {
    actions: [
        {
            authenticateOidc: {
                authorizationEndpoint: "https://example.com/authorization_endpoint",
                clientId: "client_id",
                clientSecret: "client_secret",
                issuer: "https://example.com",
                tokenEndpoint: "https://example.com/token_endpoint",
                userInfoEndpoint: "https://example.com/user_info_endpoint",
            },
            type: "authenticate-oidc",
        },
        {
            targetGroupArn: aws_lb_target_group_static.arn,
            type: "forward",
        },
    ],
    listenerArn: frontEndListener.arn,
});
```

{{% /example %}}
{{% /examples %}}



## Create a ListenerRule Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/alb/#ListenerRule">ListenerRule</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/alb/#ListenerRuleArgs">ListenerRuleArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">ListenerRule</span><span class="p">(resource_name, opts=None, </span>actions=None<span class="p">, </span>conditions=None<span class="p">, </span>listener_arn=None<span class="p">, </span>priority=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewListenerRule<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleArgs">ListenerRuleArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRule">ListenerRule</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Alb.ListenerRule.html">ListenerRule</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Alb.ListenerRuleArgs.html">ListenerRuleArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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

    <dt class="property-required"
            title="Required">
        <span>Actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleaction">List&lt;Listener<wbr>Rule<wbr>Action<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}An Action block. Action blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Conditions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerrulecondition">List&lt;Listener<wbr>Rule<wbr>Condition<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}A Condition block. Multiple condition blocks of different types can be set and all must be satisfied for the rule to match. Condition blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Listener<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the listener to which to attach the rule.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The priority for the rule between `1` and `50000`. Leaving it unset will automatically set the rule with next available priority after currently existing highest rule. A listener can't have multiple rules with the same priority.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleaction">[]Listener<wbr>Rule<wbr>Action</a></span>
    </dt>
    <dd>{{% md %}}An Action block. Action blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Conditions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerrulecondition">[]Listener<wbr>Rule<wbr>Condition</a></span>
    </dt>
    <dd>{{% md %}}A Condition block. Multiple condition blocks of different types can be set and all must be satisfied for the rule to match. Condition blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Listener<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the listener to which to attach the rule.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The priority for the rule between `1` and `50000`. Leaving it unset will automatically set the rule with next available priority after currently existing highest rule. A listener can't have multiple rules with the same priority.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleaction">Listener<wbr>Rule<wbr>Action[]</a></span>
    </dt>
    <dd>{{% md %}}An Action block. Action blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>conditions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerrulecondition">Listener<wbr>Rule<wbr>Condition[]</a></span>
    </dt>
    <dd>{{% md %}}A Condition block. Multiple condition blocks of different types can be set and all must be satisfied for the rule to match. Condition blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>listener<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the listener to which to attach the rule.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The priority for the rule between `1` and `50000`. Leaving it unset will automatically set the rule with next available priority after currently existing highest rule. A listener can't have multiple rules with the same priority.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleaction">List[Listener<wbr>Rule<wbr>Action]</a></span>
    </dt>
    <dd>{{% md %}}An Action block. Action blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>conditions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerrulecondition">List[Listener<wbr>Rule<wbr>Condition]</a></span>
    </dt>
    <dd>{{% md %}}A Condition block. Multiple condition blocks of different types can be set and all must be satisfied for the rule to match. Condition blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>listener_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the listener to which to attach the rule.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The priority for the rule between `1` and `50000`. Leaving it unset will automatically set the rule with next available priority after currently existing highest rule. A listener can't have multiple rules with the same priority.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## ListenerRule Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleaction">List&lt;Listener<wbr>Rule<wbr>Action&gt;</a></span>
    </dt>
    <dd>{{% md %}}An Action block. Action blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the rule (matches `id`)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Conditions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerrulecondition">List&lt;Listener<wbr>Rule<wbr>Condition&gt;</a></span>
    </dt>
    <dd>{{% md %}}A Condition block. Multiple condition blocks of different types can be set and all must be satisfied for the rule to match. Condition blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Listener<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the listener to which to attach the rule.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The priority for the rule between `1` and `50000`. Leaving it unset will automatically set the rule with next available priority after currently existing highest rule. A listener can't have multiple rules with the same priority.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleaction">[]Listener<wbr>Rule<wbr>Action</a></span>
    </dt>
    <dd>{{% md %}}An Action block. Action blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the rule (matches `id`)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Conditions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerrulecondition">[]Listener<wbr>Rule<wbr>Condition</a></span>
    </dt>
    <dd>{{% md %}}A Condition block. Multiple condition blocks of different types can be set and all must be satisfied for the rule to match. Condition blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Listener<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the listener to which to attach the rule.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The priority for the rule between `1` and `50000`. Leaving it unset will automatically set the rule with next available priority after currently existing highest rule. A listener can't have multiple rules with the same priority.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleaction">Listener<wbr>Rule<wbr>Action[]</a></span>
    </dt>
    <dd>{{% md %}}An Action block. Action blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the rule (matches `id`)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>conditions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerrulecondition">Listener<wbr>Rule<wbr>Condition[]</a></span>
    </dt>
    <dd>{{% md %}}A Condition block. Multiple condition blocks of different types can be set and all must be satisfied for the rule to match. Condition blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>listener<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the listener to which to attach the rule.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The priority for the rule between `1` and `50000`. Leaving it unset will automatically set the rule with next available priority after currently existing highest rule. A listener can't have multiple rules with the same priority.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleaction">List[Listener<wbr>Rule<wbr>Action]</a></span>
    </dt>
    <dd>{{% md %}}An Action block. Action blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the rule (matches `id`)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>conditions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerrulecondition">List[Listener<wbr>Rule<wbr>Condition]</a></span>
    </dt>
    <dd>{{% md %}}A Condition block. Multiple condition blocks of different types can be set and all must be satisfied for the rule to match. Condition blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>listener_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the listener to which to attach the rule.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The priority for the rule between `1` and `50000`. Leaving it unset will automatically set the rule with next available priority after currently existing highest rule. A listener can't have multiple rules with the same priority.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing ListenerRule Resource

Get an existing ListenerRule resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/alb/#ListenerRuleState">ListenerRuleState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/alb/#ListenerRule">ListenerRule</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>actions=None<span class="p">, </span>arn=None<span class="p">, </span>conditions=None<span class="p">, </span>listener_arn=None<span class="p">, </span>priority=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetListenerRule<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleState">ListenerRuleState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRule">ListenerRule</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Alb.ListenerRule.html">ListenerRule</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Alb.ListenerRuleState.html">ListenerRuleState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleaction">List&lt;Listener<wbr>Rule<wbr>Action<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}An Action block. Action blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the rule (matches `id`)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Conditions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerrulecondition">List&lt;Listener<wbr>Rule<wbr>Condition<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}A Condition block. Multiple condition blocks of different types can be set and all must be satisfied for the rule to match. Condition blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Listener<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the listener to which to attach the rule.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The priority for the rule between `1` and `50000`. Leaving it unset will automatically set the rule with next available priority after currently existing highest rule. A listener can't have multiple rules with the same priority.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleaction">[]Listener<wbr>Rule<wbr>Action</a></span>
    </dt>
    <dd>{{% md %}}An Action block. Action blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ARN of the rule (matches `id`)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Conditions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerrulecondition">[]Listener<wbr>Rule<wbr>Condition</a></span>
    </dt>
    <dd>{{% md %}}A Condition block. Multiple condition blocks of different types can be set and all must be satisfied for the rule to match. Condition blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Listener<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ARN of the listener to which to attach the rule.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The priority for the rule between `1` and `50000`. Leaving it unset will automatically set the rule with next available priority after currently existing highest rule. A listener can't have multiple rules with the same priority.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleaction">Listener<wbr>Rule<wbr>Action[]?</a></span>
    </dt>
    <dd>{{% md %}}An Action block. Action blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the rule (matches `id`)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>conditions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerrulecondition">Listener<wbr>Rule<wbr>Condition[]?</a></span>
    </dt>
    <dd>{{% md %}}A Condition block. Multiple condition blocks of different types can be set and all must be satisfied for the rule to match. Condition blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>listener<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the listener to which to attach the rule.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The priority for the rule between `1` and `50000`. Leaving it unset will automatically set the rule with next available priority after currently existing highest rule. A listener can't have multiple rules with the same priority.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>actions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleaction">List[Listener<wbr>Rule<wbr>Action]</a></span>
    </dt>
    <dd>{{% md %}}An Action block. Action blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the rule (matches `id`)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>conditions</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerrulecondition">List[Listener<wbr>Rule<wbr>Condition]</a></span>
    </dt>
    <dd>{{% md %}}A Condition block. Multiple condition blocks of different types can be set and all must be satisfied for the rule to match. Condition blocks are documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>listener_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the listener to which to attach the rule.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The priority for the rule between `1` and `50000`. Leaving it unset will automatically set the rule with next available priority after currently existing highest rule. A listener can't have multiple rules with the same priority.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Listener<wbr>Rule<wbr>Action</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#ListenerRuleAction">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#ListenerRuleAction">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleActionArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleActionOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Authenticate<wbr>Cognito</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleactionauthenticatecognito">Listener<wbr>Rule<wbr>Action<wbr>Authenticate<wbr>Cognito<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Information for creating an authenticate action using Cognito. Required if `type` is `authenticate-cognito`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authenticate<wbr>Oidc</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleactionauthenticateoidc">Listener<wbr>Rule<wbr>Action<wbr>Authenticate<wbr>Oidc<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Information for creating an authenticate action using OIDC. Required if `type` is `authenticate-oidc`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fixed<wbr>Response</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleactionfixedresponse">Listener<wbr>Rule<wbr>Action<wbr>Fixed<wbr>Response<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Information for creating an action that returns a custom HTTP response. Required if `type` is `fixed-response`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Order</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Redirect</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleactionredirect">Listener<wbr>Rule<wbr>Action<wbr>Redirect<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Information for creating a redirect action. Required if `type` is `redirect`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Group<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the Target Group to which to route traffic. Required if `type` is `forward`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of routing action. Valid values are `forward`, `redirect`, `fixed-response`, `authenticate-cognito` and `authenticate-oidc`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Authenticate<wbr>Cognito</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleactionauthenticatecognito">*Listener<wbr>Rule<wbr>Action<wbr>Authenticate<wbr>Cognito</a></span>
    </dt>
    <dd>{{% md %}}Information for creating an authenticate action using Cognito. Required if `type` is `authenticate-cognito`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Authenticate<wbr>Oidc</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleactionauthenticateoidc">*Listener<wbr>Rule<wbr>Action<wbr>Authenticate<wbr>Oidc</a></span>
    </dt>
    <dd>{{% md %}}Information for creating an authenticate action using OIDC. Required if `type` is `authenticate-oidc`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fixed<wbr>Response</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleactionfixedresponse">*Listener<wbr>Rule<wbr>Action<wbr>Fixed<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Information for creating an action that returns a custom HTTP response. Required if `type` is `fixed-response`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Order</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Redirect</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleactionredirect">*Listener<wbr>Rule<wbr>Action<wbr>Redirect</a></span>
    </dt>
    <dd>{{% md %}}Information for creating a redirect action. Required if `type` is `redirect`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target<wbr>Group<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The ARN of the Target Group to which to route traffic. Required if `type` is `forward`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of routing action. Valid values are `forward`, `redirect`, `fixed-response`, `authenticate-cognito` and `authenticate-oidc`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>authenticate<wbr>Cognito</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleactionauthenticatecognito">Listener<wbr>Rule<wbr>Action<wbr>Authenticate<wbr>Cognito?</a></span>
    </dt>
    <dd>{{% md %}}Information for creating an authenticate action using Cognito. Required if `type` is `authenticate-cognito`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authenticate<wbr>Oidc</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleactionauthenticateoidc">Listener<wbr>Rule<wbr>Action<wbr>Authenticate<wbr>Oidc?</a></span>
    </dt>
    <dd>{{% md %}}Information for creating an authenticate action using OIDC. Required if `type` is `authenticate-oidc`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fixed<wbr>Response</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleactionfixedresponse">Listener<wbr>Rule<wbr>Action<wbr>Fixed<wbr>Response?</a></span>
    </dt>
    <dd>{{% md %}}Information for creating an action that returns a custom HTTP response. Required if `type` is `fixed-response`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>order</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>redirect</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleactionredirect">Listener<wbr>Rule<wbr>Action<wbr>Redirect?</a></span>
    </dt>
    <dd>{{% md %}}Information for creating a redirect action. Required if `type` is `redirect`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target<wbr>Group<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The ARN of the Target Group to which to route traffic. Required if `type` is `forward`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of routing action. Valid values are `forward`, `redirect`, `fixed-response`, `authenticate-cognito` and `authenticate-oidc`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>authenticate<wbr>Cognito</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleactionauthenticatecognito">Dict[Listener<wbr>Rule<wbr>Action<wbr>Authenticate<wbr>Cognito]</a></span>
    </dt>
    <dd>{{% md %}}Information for creating an authenticate action using Cognito. Required if `type` is `authenticate-cognito`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>authenticate<wbr>Oidc</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleactionauthenticateoidc">Dict[Listener<wbr>Rule<wbr>Action<wbr>Authenticate<wbr>Oidc]</a></span>
    </dt>
    <dd>{{% md %}}Information for creating an authenticate action using OIDC. Required if `type` is `authenticate-oidc`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fixed<wbr>Response</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleactionfixedresponse">Dict[Listener<wbr>Rule<wbr>Action<wbr>Fixed<wbr>Response]</a></span>
    </dt>
    <dd>{{% md %}}Information for creating an action that returns a custom HTTP response. Required if `type` is `fixed-response`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>order</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>redirect</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleactionredirect">Dict[Listener<wbr>Rule<wbr>Action<wbr>Redirect]</a></span>
    </dt>
    <dd>{{% md %}}Information for creating a redirect action. Required if `type` is `redirect`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target_<wbr>group_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the Target Group to which to route traffic. Required if `type` is `forward`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of routing action. Valid values are `forward`, `redirect`, `fixed-response`, `authenticate-cognito` and `authenticate-oidc`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Listener<wbr>Rule<wbr>Action<wbr>Authenticate<wbr>Cognito</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#ListenerRuleActionAuthenticateCognito">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#ListenerRuleActionAuthenticateCognito">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleActionAuthenticateCognitoArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleActionAuthenticateCognitoOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Authentication<wbr>Request<wbr>Extra<wbr>Params</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}The query parameters to include in the redirect request to the authorization endpoint. Max: 10.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>On<wbr>Unauthenticated<wbr>Request</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The behavior if the user is not authenticated. Valid values: `deny`, `allow` and `authenticate`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The set of user claims to be requested from the IdP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Session<wbr>Cookie<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the cookie used to maintain session information.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Session<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The maximum duration of the authentication session, in seconds.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>User<wbr>Pool<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the Cognito user pool.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>User<wbr>Pool<wbr>Client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the Cognito user pool client.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>User<wbr>Pool<wbr>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The domain prefix or fully-qualified domain name of the Cognito user pool.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Authentication<wbr>Request<wbr>Extra<wbr>Params</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}The query parameters to include in the redirect request to the authorization endpoint. Max: 10.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>On<wbr>Unauthenticated<wbr>Request</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The behavior if the user is not authenticated. Valid values: `deny`, `allow` and `authenticate`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The set of user claims to be requested from the IdP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Session<wbr>Cookie<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the cookie used to maintain session information.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Session<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The maximum duration of the authentication session, in seconds.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>User<wbr>Pool<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the Cognito user pool.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>User<wbr>Pool<wbr>Client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the Cognito user pool client.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>User<wbr>Pool<wbr>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The domain prefix or fully-qualified domain name of the Cognito user pool.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>authentication<wbr>Request<wbr>Extra<wbr>Params</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}The query parameters to include in the redirect request to the authorization endpoint. Max: 10.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>on<wbr>Unauthenticated<wbr>Request</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The behavior if the user is not authenticated. Valid values: `deny`, `allow` and `authenticate`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The set of user claims to be requested from the IdP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>session<wbr>Cookie<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the cookie used to maintain session information.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>session<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The maximum duration of the authentication session, in seconds.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>user<wbr>Pool<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the Cognito user pool.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>user<wbr>Pool<wbr>Client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the Cognito user pool client.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>user<wbr>Pool<wbr>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The domain prefix or fully-qualified domain name of the Cognito user pool.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>authentication<wbr>Request<wbr>Extra<wbr>Params</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}The query parameters to include in the redirect request to the authorization endpoint. Max: 10.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>on<wbr>Unauthenticated<wbr>Request</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The behavior if the user is not authenticated. Valid values: `deny`, `allow` and `authenticate`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The set of user claims to be requested from the IdP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>session<wbr>Cookie<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the cookie used to maintain session information.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>session<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The maximum duration of the authentication session, in seconds.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>user<wbr>Pool<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the Cognito user pool.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>user<wbr>Pool<wbr>Client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the Cognito user pool client.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>user<wbr>Pool<wbr>Domain</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The domain prefix or fully-qualified domain name of the Cognito user pool.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Listener<wbr>Rule<wbr>Action<wbr>Authenticate<wbr>Oidc</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#ListenerRuleActionAuthenticateOidc">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#ListenerRuleActionAuthenticateOidc">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleActionAuthenticateOidcArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleActionAuthenticateOidcOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Authentication<wbr>Request<wbr>Extra<wbr>Params</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}The query parameters to include in the redirect request to the authorization endpoint. Max: 10.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Authorization<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The authorization endpoint of the IdP.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The OAuth 2.0 client identifier.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Client<wbr>Secret</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The OAuth 2.0 client secret.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Issuer</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The OIDC issuer identifier of the IdP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>On<wbr>Unauthenticated<wbr>Request</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The behavior if the user is not authenticated. Valid values: `deny`, `allow` and `authenticate`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The set of user claims to be requested from the IdP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Session<wbr>Cookie<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the cookie used to maintain session information.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Session<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}The maximum duration of the authentication session, in seconds.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Token<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The token endpoint of the IdP.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>User<wbr>Info<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The user info endpoint of the IdP.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Authentication<wbr>Request<wbr>Extra<wbr>Params</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}The query parameters to include in the redirect request to the authorization endpoint. Max: 10.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Authorization<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The authorization endpoint of the IdP.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The OAuth 2.0 client identifier.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Client<wbr>Secret</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The OAuth 2.0 client secret.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Issuer</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The OIDC issuer identifier of the IdP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>On<wbr>Unauthenticated<wbr>Request</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The behavior if the user is not authenticated. Valid values: `deny`, `allow` and `authenticate`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The set of user claims to be requested from the IdP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Session<wbr>Cookie<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the cookie used to maintain session information.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Session<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}The maximum duration of the authentication session, in seconds.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Token<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The token endpoint of the IdP.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>User<wbr>Info<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The user info endpoint of the IdP.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>authentication<wbr>Request<wbr>Extra<wbr>Params</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}The query parameters to include in the redirect request to the authorization endpoint. Max: 10.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>authorization<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The authorization endpoint of the IdP.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>client<wbr>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The OAuth 2.0 client identifier.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>client<wbr>Secret</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The OAuth 2.0 client secret.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>issuer</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The OIDC issuer identifier of the IdP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>on<wbr>Unauthenticated<wbr>Request</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The behavior if the user is not authenticated. Valid values: `deny`, `allow` and `authenticate`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The set of user claims to be requested from the IdP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>session<wbr>Cookie<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the cookie used to maintain session information.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>session<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}The maximum duration of the authentication session, in seconds.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>token<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The token endpoint of the IdP.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>user<wbr>Info<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The user info endpoint of the IdP.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>authentication<wbr>Request<wbr>Extra<wbr>Params</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}The query parameters to include in the redirect request to the authorization endpoint. Max: 10.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>authorization<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The authorization endpoint of the IdP.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>client_<wbr>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The OAuth 2.0 client identifier.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>client_<wbr>secret</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The OAuth 2.0 client secret.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>issuer</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The OIDC issuer identifier of the IdP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>on<wbr>Unauthenticated<wbr>Request</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The behavior if the user is not authenticated. Valid values: `deny`, `allow` and `authenticate`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>scope</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The set of user claims to be requested from the IdP.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>session<wbr>Cookie<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the cookie used to maintain session information.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>session<wbr>Timeout</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The maximum duration of the authentication session, in seconds.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>token<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The token endpoint of the IdP.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>user<wbr>Info<wbr>Endpoint</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The user info endpoint of the IdP.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Listener<wbr>Rule<wbr>Action<wbr>Fixed<wbr>Response</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#ListenerRuleActionFixedResponse">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#ListenerRuleActionFixedResponse">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleActionFixedResponseArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleActionFixedResponseOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Content<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The content type. Valid values are `text/plain`, `text/css`, `text/html`, `application/javascript` and `application/json`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Message<wbr>Body</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The message body.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Status<wbr>Code</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The HTTP response code. Valid values are `2XX`, `4XX`, or `5XX`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Content<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The content type. Valid values are `text/plain`, `text/css`, `text/html`, `application/javascript` and `application/json`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Message<wbr>Body</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The message body.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Status<wbr>Code</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The HTTP response code. Valid values are `2XX`, `4XX`, or `5XX`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>content<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The content type. Valid values are `text/plain`, `text/css`, `text/html`, `application/javascript` and `application/json`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>message<wbr>Body</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The message body.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>status<wbr>Code</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The HTTP response code. Valid values are `2XX`, `4XX`, or `5XX`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>content_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The content type. Valid values are `text/plain`, `text/css`, `text/html`, `application/javascript` and `application/json`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>message<wbr>Body</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The message body.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>status_<wbr>code</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The HTTP response code. Valid values are `2XX`, `4XX`, or `5XX`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Listener<wbr>Rule<wbr>Action<wbr>Redirect</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#ListenerRuleActionRedirect">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#ListenerRuleActionRedirect">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleActionRedirectArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleActionRedirectOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The hostname. This component is not percent-encoded. The hostname can contain `#{host}`. Defaults to `#{host}`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The absolute path, starting with the leading "/". This component is not percent-encoded. The path can contain #{host}, #{path}, and #{port}. Defaults to `/#{path}`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The port. Specify a value from `1` to `65535` or `#{port}`. Defaults to `#{port}`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The protocol. Valid values are `HTTP`, `HTTPS`, or `#{protocol}`. Defaults to `#{protocol}`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Query</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The query parameters, URL-encoded when necessary, but not percent-encoded. Do not include the leading "?". Defaults to `#{query}`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Status<wbr>Code</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The HTTP redirect code. The redirect is either permanent (`HTTP_301`) or temporary (`HTTP_302`).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Host</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The hostname. This component is not percent-encoded. The hostname can contain `#{host}`. Defaults to `#{host}`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Path</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The absolute path, starting with the leading "/". This component is not percent-encoded. The path can contain #{host}, #{path}, and #{port}. Defaults to `/#{path}`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Port</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The port. Specify a value from `1` to `65535` or `#{port}`. Defaults to `#{port}`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The protocol. Valid values are `HTTP`, `HTTPS`, or `#{protocol}`. Defaults to `#{protocol}`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Query</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The query parameters, URL-encoded when necessary, but not percent-encoded. Do not include the leading "?". Defaults to `#{query}`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Status<wbr>Code</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The HTTP redirect code. The redirect is either permanent (`HTTP_301`) or temporary (`HTTP_302`).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>host</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The hostname. This component is not percent-encoded. The hostname can contain `#{host}`. Defaults to `#{host}`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>path</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The absolute path, starting with the leading "/". This component is not percent-encoded. The path can contain #{host}, #{path}, and #{port}. Defaults to `/#{path}`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The port. Specify a value from `1` to `65535` or `#{port}`. Defaults to `#{port}`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The protocol. Valid values are `HTTP`, `HTTPS`, or `#{protocol}`. Defaults to `#{protocol}`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>query</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The query parameters, URL-encoded when necessary, but not percent-encoded. Do not include the leading "?". Defaults to `#{query}`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>status<wbr>Code</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The HTTP redirect code. The redirect is either permanent (`HTTP_301`) or temporary (`HTTP_302`).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>host</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The hostname. This component is not percent-encoded. The hostname can contain `#{host}`. Defaults to `#{host}`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>path</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The absolute path, starting with the leading "/". This component is not percent-encoded. The path can contain #{host}, #{path}, and #{port}. Defaults to `/#{path}`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>port</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The port. Specify a value from `1` to `65535` or `#{port}`. Defaults to `#{port}`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>protocol</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The protocol. Valid values are `HTTP`, `HTTPS`, or `#{protocol}`. Defaults to `#{protocol}`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>query</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The query parameters, URL-encoded when necessary, but not percent-encoded. Do not include the leading "?". Defaults to `#{query}`.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>status_<wbr>code</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The HTTP redirect code. The redirect is either permanent (`HTTP_301`) or temporary (`HTTP_302`).
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Listener<wbr>Rule<wbr>Condition</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#ListenerRuleCondition">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#ListenerRuleCondition">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleConditionArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleConditionOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>Field</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The type of condition. Valid values are `host-header` or `path-pattern`. Must also set `values`.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}use &#39;host_header&#39; or &#39;path_pattern&#39; attribute instead{{% /md %}}</p></dd>

    <dt class="property-optional"
            title="Optional">
        <span>Host<wbr>Header</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionhostheader">Listener<wbr>Rule<wbr>Condition<wbr>Host<wbr>Header<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Contains a single `values` item which is a list of host header patterns to match. The maximum size of each pattern is 128 characters. Comparison is case insensitive. Wildcard characters supported: * (matches 0 or more characters) and ? (matches exactly 1 character). Only one pattern needs to match for the condition to be satisfied.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Http<wbr>Header</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionhttpheader">Listener<wbr>Rule<wbr>Condition<wbr>Http<wbr>Header<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}HTTP headers to match. HTTP Header block fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Http<wbr>Request<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionhttprequestmethod">Listener<wbr>Rule<wbr>Condition<wbr>Http<wbr>Request<wbr>Method<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Contains a single `values` item which is a list of HTTP request methods or verbs to match. Maximum size is 40 characters. Only allowed characters are A-Z, hyphen (-) and underscore (\_). Comparison is case sensitive. Wildcards are not supported. Only one needs to match for the condition to be satisfied. AWS recommends that GET and HEAD requests are routed in the same way because the response to a HEAD request may be cached.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Path<wbr>Pattern</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionpathpattern">Listener<wbr>Rule<wbr>Condition<wbr>Path<wbr>Pattern<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Contains a single `values` item which is a list of path patterns to match against the request URL. Maximum size of each pattern is 128 characters. Comparison is case sensitive. Wildcard charaters supported: * (matches 0 or more characters) and ? (matches exactly 1 character). Only one pattern needs to match for the condition to be satisfied. Path pattern is compared only to the path of the URL, not to its query string. To compare against the query string, use a `query-string` condition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Query<wbr>Strings</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionquerystring">List&lt;Listener<wbr>Rule<wbr>Condition<wbr>Query<wbr>String<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}Query strings to match. Query String block fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Source<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionsourceip">Listener<wbr>Rule<wbr>Condition<wbr>Source<wbr>Ip<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Contains a single `values` item which is a list of source IP CIDR notations to match. You can use both IPv4 and IPv6 addresses. Wildcards are not supported. Condition is satisfied if the source IP address of the request matches one of the CIDR blocks. Condition is not satisfied by the addresses in the `X-Forwarded-For` header, use `http-header` condition instead.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}use &#39;host_header&#39; or &#39;path_pattern&#39; attribute instead{{% /md %}}</p></dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>Field</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The type of condition. Valid values are `host-header` or `path-pattern`. Must also set `values`.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}use &#39;host_header&#39; or &#39;path_pattern&#39; attribute instead{{% /md %}}</p></dd>

    <dt class="property-optional"
            title="Optional">
        <span>Host<wbr>Header</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionhostheader">*Listener<wbr>Rule<wbr>Condition<wbr>Host<wbr>Header</a></span>
    </dt>
    <dd>{{% md %}}Contains a single `values` item which is a list of host header patterns to match. The maximum size of each pattern is 128 characters. Comparison is case insensitive. Wildcard characters supported: * (matches 0 or more characters) and ? (matches exactly 1 character). Only one pattern needs to match for the condition to be satisfied.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Http<wbr>Header</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionhttpheader">*Listener<wbr>Rule<wbr>Condition<wbr>Http<wbr>Header</a></span>
    </dt>
    <dd>{{% md %}}HTTP headers to match. HTTP Header block fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Http<wbr>Request<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionhttprequestmethod">*Listener<wbr>Rule<wbr>Condition<wbr>Http<wbr>Request<wbr>Method</a></span>
    </dt>
    <dd>{{% md %}}Contains a single `values` item which is a list of HTTP request methods or verbs to match. Maximum size is 40 characters. Only allowed characters are A-Z, hyphen (-) and underscore (\_). Comparison is case sensitive. Wildcards are not supported. Only one needs to match for the condition to be satisfied. AWS recommends that GET and HEAD requests are routed in the same way because the response to a HEAD request may be cached.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Path<wbr>Pattern</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionpathpattern">*Listener<wbr>Rule<wbr>Condition<wbr>Path<wbr>Pattern</a></span>
    </dt>
    <dd>{{% md %}}Contains a single `values` item which is a list of path patterns to match against the request URL. Maximum size of each pattern is 128 characters. Comparison is case sensitive. Wildcard charaters supported: * (matches 0 or more characters) and ? (matches exactly 1 character). Only one pattern needs to match for the condition to be satisfied. Path pattern is compared only to the path of the URL, not to its query string. To compare against the query string, use a `query-string` condition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Query<wbr>Strings</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionquerystring">[]Listener<wbr>Rule<wbr>Condition<wbr>Query<wbr>String</a></span>
    </dt>
    <dd>{{% md %}}Query strings to match. Query String block fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Source<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionsourceip">*Listener<wbr>Rule<wbr>Condition<wbr>Source<wbr>Ip</a></span>
    </dt>
    <dd>{{% md %}}Contains a single `values` item which is a list of source IP CIDR notations to match. You can use both IPv4 and IPv6 addresses. Wildcards are not supported. Condition is satisfied if the source IP address of the request matches one of the CIDR blocks. Condition is not satisfied by the addresses in the `X-Forwarded-For` header, use `http-header` condition instead.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}use &#39;host_header&#39; or &#39;path_pattern&#39; attribute instead{{% /md %}}</p></dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>field</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The type of condition. Valid values are `host-header` or `path-pattern`. Must also set `values`.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}use &#39;host_header&#39; or &#39;path_pattern&#39; attribute instead{{% /md %}}</p></dd>

    <dt class="property-optional"
            title="Optional">
        <span>host<wbr>Header</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionhostheader">Listener<wbr>Rule<wbr>Condition<wbr>Host<wbr>Header?</a></span>
    </dt>
    <dd>{{% md %}}Contains a single `values` item which is a list of host header patterns to match. The maximum size of each pattern is 128 characters. Comparison is case insensitive. Wildcard characters supported: * (matches 0 or more characters) and ? (matches exactly 1 character). Only one pattern needs to match for the condition to be satisfied.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>http<wbr>Header</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionhttpheader">Listener<wbr>Rule<wbr>Condition<wbr>Http<wbr>Header?</a></span>
    </dt>
    <dd>{{% md %}}HTTP headers to match. HTTP Header block fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>http<wbr>Request<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionhttprequestmethod">Listener<wbr>Rule<wbr>Condition<wbr>Http<wbr>Request<wbr>Method?</a></span>
    </dt>
    <dd>{{% md %}}Contains a single `values` item which is a list of HTTP request methods or verbs to match. Maximum size is 40 characters. Only allowed characters are A-Z, hyphen (-) and underscore (\_). Comparison is case sensitive. Wildcards are not supported. Only one needs to match for the condition to be satisfied. AWS recommends that GET and HEAD requests are routed in the same way because the response to a HEAD request may be cached.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>path<wbr>Pattern</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionpathpattern">Listener<wbr>Rule<wbr>Condition<wbr>Path<wbr>Pattern?</a></span>
    </dt>
    <dd>{{% md %}}Contains a single `values` item which is a list of path patterns to match against the request URL. Maximum size of each pattern is 128 characters. Comparison is case sensitive. Wildcard charaters supported: * (matches 0 or more characters) and ? (matches exactly 1 character). Only one pattern needs to match for the condition to be satisfied. Path pattern is compared only to the path of the URL, not to its query string. To compare against the query string, use a `query-string` condition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>query<wbr>Strings</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionquerystring">Listener<wbr>Rule<wbr>Condition<wbr>Query<wbr>String[]?</a></span>
    </dt>
    <dd>{{% md %}}Query strings to match. Query String block fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>source<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionsourceip">Listener<wbr>Rule<wbr>Condition<wbr>Source<wbr>Ip?</a></span>
    </dt>
    <dd>{{% md %}}Contains a single `values` item which is a list of source IP CIDR notations to match. You can use both IPv4 and IPv6 addresses. Wildcards are not supported. Condition is satisfied if the source IP address of the request matches one of the CIDR blocks. Condition is not satisfied by the addresses in the `X-Forwarded-For` header, use `http-header` condition instead.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}use &#39;host_header&#39; or &#39;path_pattern&#39; attribute instead{{% /md %}}</p></dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>field</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of condition. Valid values are `host-header` or `path-pattern`. Must also set `values`.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}use &#39;host_header&#39; or &#39;path_pattern&#39; attribute instead{{% /md %}}</p></dd>

    <dt class="property-optional"
            title="Optional">
        <span>host<wbr>Header</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionhostheader">Dict[Listener<wbr>Rule<wbr>Condition<wbr>Host<wbr>Header]</a></span>
    </dt>
    <dd>{{% md %}}Contains a single `values` item which is a list of host header patterns to match. The maximum size of each pattern is 128 characters. Comparison is case insensitive. Wildcard characters supported: * (matches 0 or more characters) and ? (matches exactly 1 character). Only one pattern needs to match for the condition to be satisfied.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>http<wbr>Header</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionhttpheader">Dict[Listener<wbr>Rule<wbr>Condition<wbr>Http<wbr>Header]</a></span>
    </dt>
    <dd>{{% md %}}HTTP headers to match. HTTP Header block fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>http<wbr>Request<wbr>Method</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionhttprequestmethod">Dict[Listener<wbr>Rule<wbr>Condition<wbr>Http<wbr>Request<wbr>Method]</a></span>
    </dt>
    <dd>{{% md %}}Contains a single `values` item which is a list of HTTP request methods or verbs to match. Maximum size is 40 characters. Only allowed characters are A-Z, hyphen (-) and underscore (\_). Comparison is case sensitive. Wildcards are not supported. Only one needs to match for the condition to be satisfied. AWS recommends that GET and HEAD requests are routed in the same way because the response to a HEAD request may be cached.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>path<wbr>Pattern</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionpathpattern">Dict[Listener<wbr>Rule<wbr>Condition<wbr>Path<wbr>Pattern]</a></span>
    </dt>
    <dd>{{% md %}}Contains a single `values` item which is a list of path patterns to match against the request URL. Maximum size of each pattern is 128 characters. Comparison is case sensitive. Wildcard charaters supported: * (matches 0 or more characters) and ? (matches exactly 1 character). Only one pattern needs to match for the condition to be satisfied. Path pattern is compared only to the path of the URL, not to its query string. To compare against the query string, use a `query-string` condition.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>query<wbr>Strings</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionquerystring">List[Listener<wbr>Rule<wbr>Condition<wbr>Query<wbr>String]</a></span>
    </dt>
    <dd>{{% md %}}Query strings to match. Query String block fields documented below.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>source<wbr>Ip</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#listenerruleconditionsourceip">Dict[Listener<wbr>Rule<wbr>Condition<wbr>Source<wbr>Ip]</a></span>
    </dt>
    <dd>{{% md %}}Contains a single `values` item which is a list of source IP CIDR notations to match. You can use both IPv4 and IPv6 addresses. Wildcards are not supported. Condition is satisfied if the source IP address of the request matches one of the CIDR blocks. Condition is not satisfied by the addresses in the `X-Forwarded-For` header, use `http-header` condition instead.
{{% /md %}}</dd>

    <dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}<p class="property-message">Deprecated: {{% md %}}use &#39;host_header&#39; or &#39;path_pattern&#39; attribute instead{{% /md %}}</p></dd>

</dl>
{{% /choosable %}}





<h4>Listener<wbr>Rule<wbr>Condition<wbr>Host<wbr>Header</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#ListenerRuleConditionHostHeader">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#ListenerRuleConditionHostHeader">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleConditionHostHeaderArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleConditionHostHeaderOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Listener<wbr>Rule<wbr>Condition<wbr>Http<wbr>Header</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#ListenerRuleConditionHttpHeader">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#ListenerRuleConditionHttpHeader">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleConditionHttpHeaderArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleConditionHttpHeaderOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Http<wbr>Header<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of HTTP header to search. The maximum size is 40 characters. Comparison is case insensitive. Only RFC7240 characters are supported. Wildcards are not supported. You cannot use HTTP header condition to specify the host header, use a `host-header` condition instead.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}List of header value patterns to match. Maximum size of each pattern is 128 characters. Comparison is case insensitive. Wildcard characters supported: * (matches 0 or more characters) and ? (matches exactly 1 character). If the same header appears multiple times in the request they will be searched in order until a match is found. Only one pattern needs to match for the condition to be satisfied. To require that all of the strings are a match, create one condition block per string.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Http<wbr>Header<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of HTTP header to search. The maximum size is 40 characters. Comparison is case insensitive. Only RFC7240 characters are supported. Wildcards are not supported. You cannot use HTTP header condition to specify the host header, use a `host-header` condition instead.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of header value patterns to match. Maximum size of each pattern is 128 characters. Comparison is case insensitive. Wildcard characters supported: * (matches 0 or more characters) and ? (matches exactly 1 character). If the same header appears multiple times in the request they will be searched in order until a match is found. Only one pattern needs to match for the condition to be satisfied. To require that all of the strings are a match, create one condition block per string.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>http<wbr>Header<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of HTTP header to search. The maximum size is 40 characters. Comparison is case insensitive. Only RFC7240 characters are supported. Wildcards are not supported. You cannot use HTTP header condition to specify the host header, use a `host-header` condition instead.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}List of header value patterns to match. Maximum size of each pattern is 128 characters. Comparison is case insensitive. Wildcard characters supported: * (matches 0 or more characters) and ? (matches exactly 1 character). If the same header appears multiple times in the request they will be searched in order until a match is found. Only one pattern needs to match for the condition to be satisfied. To require that all of the strings are a match, create one condition block per string.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>http<wbr>Header<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of HTTP header to search. The maximum size is 40 characters. Comparison is case insensitive. Only RFC7240 characters are supported. Wildcards are not supported. You cannot use HTTP header condition to specify the host header, use a `host-header` condition instead.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}List of header value patterns to match. Maximum size of each pattern is 128 characters. Comparison is case insensitive. Wildcard characters supported: * (matches 0 or more characters) and ? (matches exactly 1 character). If the same header appears multiple times in the request they will be searched in order until a match is found. Only one pattern needs to match for the condition to be satisfied. To require that all of the strings are a match, create one condition block per string.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Listener<wbr>Rule<wbr>Condition<wbr>Http<wbr>Request<wbr>Method</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#ListenerRuleConditionHttpRequestMethod">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#ListenerRuleConditionHttpRequestMethod">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleConditionHttpRequestMethodArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleConditionHttpRequestMethodOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Listener<wbr>Rule<wbr>Condition<wbr>Path<wbr>Pattern</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#ListenerRuleConditionPathPattern">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#ListenerRuleConditionPathPattern">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleConditionPathPatternArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleConditionPathPatternOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Listener<wbr>Rule<wbr>Condition<wbr>Query<wbr>String</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#ListenerRuleConditionQueryString">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#ListenerRuleConditionQueryString">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleConditionQueryStringArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleConditionQueryStringOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Query string key pattern to match.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Query string value pattern to match.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Key</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Query string key pattern to match.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Query string value pattern to match.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>key</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Query string key pattern to match.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Query string value pattern to match.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>key</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Query string key pattern to match.
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Query string value pattern to match.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Listener<wbr>Rule<wbr>Condition<wbr>Source<wbr>Ip</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#ListenerRuleConditionSourceIp">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#ListenerRuleConditionSourceIp">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleConditionSourceIpArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/alb?tab=doc#ListenerRuleConditionSourceIpOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Values</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>values</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}List of exactly one pattern to match. Required when `field` is set.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-aws">https://github.com/pulumi/pulumi-aws</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    <dt>Notes</dt>
	<dd>This Pulumi package is based on the [`aws` Terraform Provider](https://github.com/terraform-providers/terraform-provider-aws).</dd>
</dl>

