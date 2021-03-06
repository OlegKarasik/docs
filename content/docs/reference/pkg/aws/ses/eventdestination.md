
---
title: "EventDestination"
block_external_search_index: true
---



Provides an SES event destination

{{% examples %}}
## Example Usage

{{% example %}}
### CloudWatch Destination

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const cloudwatch = new aws.ses.EventDestination("cloudwatch", {
    cloudwatchDestinations: [{
        defaultValue: "default",
        dimensionName: "dimension",
        valueSource: "emailHeader",
    }],
    configurationSetName: aws_ses_configuration_set_example.name,
    enabled: true,
    matchingTypes: [
        "bounce",
        "send",
    ],
});
```

{{% /example %}}
{{% example %}}
### Kinesis Destination

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const kinesis = new aws.ses.EventDestination("kinesis", {
    configurationSetName: aws_ses_configuration_set_example.name,
    enabled: true,
    kinesisDestination: {
        roleArn: aws_iam_role_example.arn,
        streamArn: aws_kinesis_firehose_delivery_stream_example.arn,
    },
    matchingTypes: [
        "bounce",
        "send",
    ],
});
```

{{% /example %}}
{{% example %}}
### SNS Destination

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const sns = new aws.ses.EventDestination("sns", {
    configurationSetName: aws_ses_configuration_set_example.name,
    enabled: true,
    matchingTypes: [
        "bounce",
        "send",
    ],
    snsDestination: {
        topicArn: aws_sns_topic_example.arn,
    },
});
```

{{% /example %}}
{{% /examples %}}



## Create a EventDestination Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/ses/#EventDestination">EventDestination</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/ses/#EventDestinationArgs">EventDestinationArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">EventDestination</span><span class="p">(resource_name, opts=None, </span>cloudwatch_destinations=None<span class="p">, </span>configuration_set_name=None<span class="p">, </span>enabled=None<span class="p">, </span>kinesis_destination=None<span class="p">, </span>matching_types=None<span class="p">, </span>name=None<span class="p">, </span>sns_destination=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewEventDestination<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ses?tab=doc#EventDestinationArgs">EventDestinationArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ses?tab=doc#EventDestination">EventDestination</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Ses.EventDestination.html">EventDestination</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Ses.EventDestinationArgs.html">EventDestinationArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Cloudwatch<wbr>Destinations</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationcloudwatchdestination">List&lt;Event<wbr>Destination<wbr>Cloudwatch<wbr>Destination<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}CloudWatch destination for the events
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Configuration<wbr>Set<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the configuration set
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}If true, the event destination will be enabled
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kinesis<wbr>Destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationkinesisdestination">Event<wbr>Destination<wbr>Kinesis<wbr>Destination<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Send the events to a kinesis firehose destination
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Matching<wbr>Types</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}A list of matching types. May be any of `"send"`, `"reject"`, `"bounce"`, `"complaint"`, `"delivery"`, `"open"`, `"click"`, or `"renderingFailure"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the event destination
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sns<wbr>Destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationsnsdestination">Event<wbr>Destination<wbr>Sns<wbr>Destination<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Send the events to an SNS Topic destination
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Cloudwatch<wbr>Destinations</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationcloudwatchdestination">[]Event<wbr>Destination<wbr>Cloudwatch<wbr>Destination</a></span>
    </dt>
    <dd>{{% md %}}CloudWatch destination for the events
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Configuration<wbr>Set<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the configuration set
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}If true, the event destination will be enabled
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kinesis<wbr>Destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationkinesisdestination">*Event<wbr>Destination<wbr>Kinesis<wbr>Destination</a></span>
    </dt>
    <dd>{{% md %}}Send the events to a kinesis firehose destination
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Matching<wbr>Types</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of matching types. May be any of `"send"`, `"reject"`, `"bounce"`, `"complaint"`, `"delivery"`, `"open"`, `"click"`, or `"renderingFailure"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the event destination
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sns<wbr>Destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationsnsdestination">*Event<wbr>Destination<wbr>Sns<wbr>Destination</a></span>
    </dt>
    <dd>{{% md %}}Send the events to an SNS Topic destination
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>cloudwatch<wbr>Destinations</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationcloudwatchdestination">Event<wbr>Destination<wbr>Cloudwatch<wbr>Destination[]?</a></span>
    </dt>
    <dd>{{% md %}}CloudWatch destination for the events
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>configuration<wbr>Set<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the configuration set
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}If true, the event destination will be enabled
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kinesis<wbr>Destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationkinesisdestination">Event<wbr>Destination<wbr>Kinesis<wbr>Destination?</a></span>
    </dt>
    <dd>{{% md %}}Send the events to a kinesis firehose destination
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>matching<wbr>Types</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of matching types. May be any of `"send"`, `"reject"`, `"bounce"`, `"complaint"`, `"delivery"`, `"open"`, `"click"`, or `"renderingFailure"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the event destination
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sns<wbr>Destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationsnsdestination">Event<wbr>Destination<wbr>Sns<wbr>Destination?</a></span>
    </dt>
    <dd>{{% md %}}Send the events to an SNS Topic destination
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>cloudwatch_<wbr>destinations</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationcloudwatchdestination">List[Event<wbr>Destination<wbr>Cloudwatch<wbr>Destination]</a></span>
    </dt>
    <dd>{{% md %}}CloudWatch destination for the events
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>configuration_<wbr>set_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the configuration set
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true, the event destination will be enabled
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kinesis_<wbr>destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationkinesisdestination">Dict[Event<wbr>Destination<wbr>Kinesis<wbr>Destination]</a></span>
    </dt>
    <dd>{{% md %}}Send the events to a kinesis firehose destination
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>matching_<wbr>types</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of matching types. May be any of `"send"`, `"reject"`, `"bounce"`, `"complaint"`, `"delivery"`, `"open"`, `"click"`, or `"renderingFailure"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the event destination
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sns_<wbr>destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationsnsdestination">Dict[Event<wbr>Destination<wbr>Sns<wbr>Destination]</a></span>
    </dt>
    <dd>{{% md %}}Send the events to an SNS Topic destination
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## EventDestination Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Cloudwatch<wbr>Destinations</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationcloudwatchdestination">List&lt;Event<wbr>Destination<wbr>Cloudwatch<wbr>Destination&gt;?</a></span>
    </dt>
    <dd>{{% md %}}CloudWatch destination for the events
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Configuration<wbr>Set<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the configuration set
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}If true, the event destination will be enabled
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Kinesis<wbr>Destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationkinesisdestination">Event<wbr>Destination<wbr>Kinesis<wbr>Destination?</a></span>
    </dt>
    <dd>{{% md %}}Send the events to a kinesis firehose destination
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Matching<wbr>Types</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string></span>
    </dt>
    <dd>{{% md %}}A list of matching types. May be any of `"send"`, `"reject"`, `"bounce"`, `"complaint"`, `"delivery"`, `"open"`, `"click"`, or `"renderingFailure"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the event destination
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Sns<wbr>Destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationsnsdestination">Event<wbr>Destination<wbr>Sns<wbr>Destination?</a></span>
    </dt>
    <dd>{{% md %}}Send the events to an SNS Topic destination
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Cloudwatch<wbr>Destinations</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationcloudwatchdestination">[]Event<wbr>Destination<wbr>Cloudwatch<wbr>Destination</a></span>
    </dt>
    <dd>{{% md %}}CloudWatch destination for the events
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Configuration<wbr>Set<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the configuration set
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}If true, the event destination will be enabled
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Kinesis<wbr>Destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationkinesisdestination">*Event<wbr>Destination<wbr>Kinesis<wbr>Destination</a></span>
    </dt>
    <dd>{{% md %}}Send the events to a kinesis firehose destination
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Matching<wbr>Types</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of matching types. May be any of `"send"`, `"reject"`, `"bounce"`, `"complaint"`, `"delivery"`, `"open"`, `"click"`, or `"renderingFailure"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the event destination
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Sns<wbr>Destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationsnsdestination">*Event<wbr>Destination<wbr>Sns<wbr>Destination</a></span>
    </dt>
    <dd>{{% md %}}Send the events to an SNS Topic destination
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>cloudwatch<wbr>Destinations</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationcloudwatchdestination">Event<wbr>Destination<wbr>Cloudwatch<wbr>Destination[]?</a></span>
    </dt>
    <dd>{{% md %}}CloudWatch destination for the events
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>configuration<wbr>Set<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the configuration set
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}If true, the event destination will be enabled
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>kinesis<wbr>Destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationkinesisdestination">Event<wbr>Destination<wbr>Kinesis<wbr>Destination?</a></span>
    </dt>
    <dd>{{% md %}}Send the events to a kinesis firehose destination
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>matching<wbr>Types</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of matching types. May be any of `"send"`, `"reject"`, `"bounce"`, `"complaint"`, `"delivery"`, `"open"`, `"click"`, or `"renderingFailure"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the event destination
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>sns<wbr>Destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationsnsdestination">Event<wbr>Destination<wbr>Sns<wbr>Destination?</a></span>
    </dt>
    <dd>{{% md %}}Send the events to an SNS Topic destination
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>cloudwatch_<wbr>destinations</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationcloudwatchdestination">List[Event<wbr>Destination<wbr>Cloudwatch<wbr>Destination]</a></span>
    </dt>
    <dd>{{% md %}}CloudWatch destination for the events
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>configuration_<wbr>set_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the configuration set
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true, the event destination will be enabled
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>kinesis_<wbr>destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationkinesisdestination">Dict[Event<wbr>Destination<wbr>Kinesis<wbr>Destination]</a></span>
    </dt>
    <dd>{{% md %}}Send the events to a kinesis firehose destination
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>matching_<wbr>types</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of matching types. May be any of `"send"`, `"reject"`, `"bounce"`, `"complaint"`, `"delivery"`, `"open"`, `"click"`, or `"renderingFailure"`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the event destination
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>sns_<wbr>destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationsnsdestination">Dict[Event<wbr>Destination<wbr>Sns<wbr>Destination]</a></span>
    </dt>
    <dd>{{% md %}}Send the events to an SNS Topic destination
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing EventDestination Resource

Get an existing EventDestination resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/ses/#EventDestinationState">EventDestinationState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/ses/#EventDestination">EventDestination</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>cloudwatch_destinations=None<span class="p">, </span>configuration_set_name=None<span class="p">, </span>enabled=None<span class="p">, </span>kinesis_destination=None<span class="p">, </span>matching_types=None<span class="p">, </span>name=None<span class="p">, </span>sns_destination=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetEventDestination<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ses?tab=doc#EventDestinationState">EventDestinationState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ses?tab=doc#EventDestination">EventDestination</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Ses.EventDestination.html">EventDestination</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Ses.EventDestinationState.html">EventDestinationState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Cloudwatch<wbr>Destinations</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationcloudwatchdestination">List&lt;Event<wbr>Destination<wbr>Cloudwatch<wbr>Destination<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}CloudWatch destination for the events
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Configuration<wbr>Set<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the configuration set
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool?</span>
    </dt>
    <dd>{{% md %}}If true, the event destination will be enabled
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kinesis<wbr>Destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationkinesisdestination">Event<wbr>Destination<wbr>Kinesis<wbr>Destination<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Send the events to a kinesis firehose destination
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Matching<wbr>Types</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}A list of matching types. May be any of `"send"`, `"reject"`, `"bounce"`, `"complaint"`, `"delivery"`, `"open"`, `"click"`, or `"renderingFailure"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the event destination
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sns<wbr>Destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationsnsdestination">Event<wbr>Destination<wbr>Sns<wbr>Destination<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Send the events to an SNS Topic destination
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Cloudwatch<wbr>Destinations</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationcloudwatchdestination">[]Event<wbr>Destination<wbr>Cloudwatch<wbr>Destination</a></span>
    </dt>
    <dd>{{% md %}}CloudWatch destination for the events
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Configuration<wbr>Set<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the configuration set
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">*bool</span>
    </dt>
    <dd>{{% md %}}If true, the event destination will be enabled
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Kinesis<wbr>Destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationkinesisdestination">*Event<wbr>Destination<wbr>Kinesis<wbr>Destination</a></span>
    </dt>
    <dd>{{% md %}}Send the events to a kinesis firehose destination
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Matching<wbr>Types</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of matching types. May be any of `"send"`, `"reject"`, `"bounce"`, `"complaint"`, `"delivery"`, `"open"`, `"click"`, or `"renderingFailure"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the event destination
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sns<wbr>Destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationsnsdestination">*Event<wbr>Destination<wbr>Sns<wbr>Destination</a></span>
    </dt>
    <dd>{{% md %}}Send the events to an SNS Topic destination
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>cloudwatch<wbr>Destinations</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationcloudwatchdestination">Event<wbr>Destination<wbr>Cloudwatch<wbr>Destination[]?</a></span>
    </dt>
    <dd>{{% md %}}CloudWatch destination for the events
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>configuration<wbr>Set<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the configuration set
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean?</span>
    </dt>
    <dd>{{% md %}}If true, the event destination will be enabled
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kinesis<wbr>Destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationkinesisdestination">Event<wbr>Destination<wbr>Kinesis<wbr>Destination?</a></span>
    </dt>
    <dd>{{% md %}}Send the events to a kinesis firehose destination
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>matching<wbr>Types</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}A list of matching types. May be any of `"send"`, `"reject"`, `"bounce"`, `"complaint"`, `"delivery"`, `"open"`, `"click"`, or `"renderingFailure"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the event destination
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sns<wbr>Destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationsnsdestination">Event<wbr>Destination<wbr>Sns<wbr>Destination?</a></span>
    </dt>
    <dd>{{% md %}}Send the events to an SNS Topic destination
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>cloudwatch_<wbr>destinations</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationcloudwatchdestination">List[Event<wbr>Destination<wbr>Cloudwatch<wbr>Destination]</a></span>
    </dt>
    <dd>{{% md %}}CloudWatch destination for the events
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>configuration_<wbr>set_<wbr>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the configuration set
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enabled</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}If true, the event destination will be enabled
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>kinesis_<wbr>destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationkinesisdestination">Dict[Event<wbr>Destination<wbr>Kinesis<wbr>Destination]</a></span>
    </dt>
    <dd>{{% md %}}Send the events to a kinesis firehose destination
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>matching_<wbr>types</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}A list of matching types. May be any of `"send"`, `"reject"`, `"bounce"`, `"complaint"`, `"delivery"`, `"open"`, `"click"`, or `"renderingFailure"`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the event destination
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sns_<wbr>destination</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#eventdestinationsnsdestination">Dict[Event<wbr>Destination<wbr>Sns<wbr>Destination]</a></span>
    </dt>
    <dd>{{% md %}}Send the events to an SNS Topic destination
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Event<wbr>Destination<wbr>Cloudwatch<wbr>Destination</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#EventDestinationCloudwatchDestination">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#EventDestinationCloudwatchDestination">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ses?tab=doc#EventDestinationCloudwatchDestinationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ses?tab=doc#EventDestinationCloudwatchDestinationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Default<wbr>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The default value for the event
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Dimension<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name for the dimension
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Value<wbr>Source</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The source for the value. It can be either `"messageTag"` or `"emailHeader"`
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Default<wbr>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The default value for the event
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Dimension<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name for the dimension
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Value<wbr>Source</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The source for the value. It can be either `"messageTag"` or `"emailHeader"`
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>default<wbr>Value</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The default value for the event
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>dimension<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name for the dimension
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>value<wbr>Source</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The source for the value. It can be either `"messageTag"` or `"emailHeader"`
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>default_<wbr>value</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The default value for the event
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>dimension<wbr>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name for the dimension
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>value<wbr>Source</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The source for the value. It can be either `"messageTag"` or `"emailHeader"`
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Event<wbr>Destination<wbr>Kinesis<wbr>Destination</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#EventDestinationKinesisDestination">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#EventDestinationKinesisDestination">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ses?tab=doc#EventDestinationKinesisDestinationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ses?tab=doc#EventDestinationKinesisDestinationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the role that has permissions to access the Kinesis Stream
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Stream<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the Kinesis Stream
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the role that has permissions to access the Kinesis Stream
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Stream<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the Kinesis Stream
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>role<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the role that has permissions to access the Kinesis Stream
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>stream<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the Kinesis Stream
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>role_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the role that has permissions to access the Kinesis Stream
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>stream_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the Kinesis Stream
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Event<wbr>Destination<wbr>Sns<wbr>Destination</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#EventDestinationSnsDestination">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#EventDestinationSnsDestination">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ses?tab=doc#EventDestinationSnsDestinationArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/ses?tab=doc#EventDestinationSnsDestinationOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Topic<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the SNS topic
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>Topic<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the SNS topic
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>topic<wbr>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the SNS topic
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-required"
            title="Required">
        <span>topic_<wbr>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the SNS topic
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

