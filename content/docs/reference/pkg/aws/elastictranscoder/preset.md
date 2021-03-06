
---
title: "Preset"
block_external_search_index: true
---



Provides an Elastic Transcoder preset resource.

{{% examples %}}
## Example Usage
{{% example %}}

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const bar = new aws.elastictranscoder.Preset("bar", {
    audio: {
        audioPackingMode: "SingleTrack",
        bitRate: "96",
        channels: "2",
        codec: "AAC",
        sampleRate: "44100",
    },
    audioCodecOptions: {
        profile: "AAC-LC",
    },
    container: "mp4",
    description: "Sample Preset",
    thumbnails: {
        format: "png",
        interval: "120",
        maxHeight: "auto",
        maxWidth: "auto",
        paddingPolicy: "Pad",
        sizingPolicy: "Fit",
    },
    video: {
        bitRate: "1600",
        codec: "H.264",
        displayAspectRatio: "16:9",
        fixedGop: "false",
        frameRate: "auto",
        keyframesMaxDist: "240",
        maxFrameRate: "60",
        maxHeight: "auto",
        maxWidth: "auto",
        paddingPolicy: "Pad",
        sizingPolicy: "Fit",
    },
    videoCodecOptions: {
        ColorSpaceConversionMode: "None",
        InterlacedMode: "Progressive",
        Level: "2.2",
        MaxReferenceFrames: 3,
        Profile: "main",
    },
    videoWatermarks: [{
        horizontalAlign: "Right",
        horizontalOffset: "10px",
        id: "Test",
        maxHeight: "20%",
        maxWidth: "20%",
        opacity: "55.5",
        sizingPolicy: "ShrinkToFit",
        target: "Content",
        verticalAlign: "Bottom",
        verticalOffset: "10px",
    }],
});
```

{{% /example %}}
{{% /examples %}}



## Create a Preset Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/elastictranscoder/#Preset">Preset</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/elastictranscoder/#PresetArgs">PresetArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">Preset</span><span class="p">(resource_name, opts=None, </span>audio=None<span class="p">, </span>audio_codec_options=None<span class="p">, </span>container=None<span class="p">, </span>description=None<span class="p">, </span>name=None<span class="p">, </span>thumbnails=None<span class="p">, </span>type=None<span class="p">, </span>video=None<span class="p">, </span>video_codec_options=None<span class="p">, </span>video_watermarks=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewPreset<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/elastictranscoder?tab=doc#PresetArgs">PresetArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/elastictranscoder?tab=doc#Preset">Preset</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Elastictranscoder.Preset.html">Preset</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.ElasticTranscoder.PresetArgs.html">PresetArgs</a></span> <span class="nx">args<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Audio</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudio">Preset<wbr>Audio<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Audio parameters object (documented below).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Audio<wbr>Codec<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudiocodecoptions">Preset<wbr>Audio<wbr>Codec<wbr>Options<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Codec options for the audio parameters (documented below)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Container</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The container type for the output file. Valid values are `flac`, `flv`, `fmp4`, `gif`, `mp3`, `mp4`, `mpg`, `mxf`, `oga`, `ogg`, `ts`, and `webm`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A description of the preset (maximum 255 characters)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the preset. (maximum 40 characters)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Thumbnails</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetthumbnails">Preset<wbr>Thumbnails<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Thumbnail parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Video</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideo">Preset<wbr>Video<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Video parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Video<wbr>Codec<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Video<wbr>Watermarks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideowatermark">List&lt;Preset<wbr>Video<wbr>Watermark<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}Watermark parameters for the video parameters (documented below)
* `video_codec_options` (Optional, Forces new resource) Codec options for the video parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Audio</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudio">*Preset<wbr>Audio</a></span>
    </dt>
    <dd>{{% md %}}Audio parameters object (documented below).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Audio<wbr>Codec<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudiocodecoptions">*Preset<wbr>Audio<wbr>Codec<wbr>Options</a></span>
    </dt>
    <dd>{{% md %}}Codec options for the audio parameters (documented below)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>Container</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The container type for the output file. Valid values are `flac`, `flv`, `fmp4`, `gif`, `mp3`, `mp4`, `mpg`, `mxf`, `oga`, `ogg`, `ts`, and `webm`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A description of the preset (maximum 255 characters)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the preset. (maximum 40 characters)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Thumbnails</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetthumbnails">*Preset<wbr>Thumbnails</a></span>
    </dt>
    <dd>{{% md %}}Thumbnail parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Video</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideo">*Preset<wbr>Video</a></span>
    </dt>
    <dd>{{% md %}}Video parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Video<wbr>Codec<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Video<wbr>Watermarks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideowatermark">[]Preset<wbr>Video<wbr>Watermark</a></span>
    </dt>
    <dd>{{% md %}}Watermark parameters for the video parameters (documented below)
* `video_codec_options` (Optional, Forces new resource) Codec options for the video parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>audio</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudio">Preset<wbr>Audio?</a></span>
    </dt>
    <dd>{{% md %}}Audio parameters object (documented below).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>audio<wbr>Codec<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudiocodecoptions">Preset<wbr>Audio<wbr>Codec<wbr>Options?</a></span>
    </dt>
    <dd>{{% md %}}Codec options for the audio parameters (documented below)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>container</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The container type for the output file. Valid values are `flac`, `flv`, `fmp4`, `gif`, `mp3`, `mp4`, `mpg`, `mxf`, `oga`, `ogg`, `ts`, and `webm`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A description of the preset (maximum 255 characters)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the preset. (maximum 40 characters)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>thumbnails</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetthumbnails">Preset<wbr>Thumbnails?</a></span>
    </dt>
    <dd>{{% md %}}Thumbnail parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>video</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideo">Preset<wbr>Video?</a></span>
    </dt>
    <dd>{{% md %}}Video parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>video<wbr>Codec<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>video<wbr>Watermarks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideowatermark">Preset<wbr>Video<wbr>Watermark[]?</a></span>
    </dt>
    <dd>{{% md %}}Watermark parameters for the video parameters (documented below)
* `video_codec_options` (Optional, Forces new resource) Codec options for the video parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>audio</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudio">Dict[Preset<wbr>Audio]</a></span>
    </dt>
    <dd>{{% md %}}Audio parameters object (documented below).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>audio_<wbr>codec_<wbr>options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudiocodecoptions">Dict[Preset<wbr>Audio<wbr>Codec<wbr>Options]</a></span>
    </dt>
    <dd>{{% md %}}Codec options for the audio parameters (documented below)
{{% /md %}}</dd>

    <dt class="property-required"
            title="Required">
        <span>container</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The container type for the output file. Valid values are `flac`, `flv`, `fmp4`, `gif`, `mp3`, `mp4`, `mpg`, `mxf`, `oga`, `ogg`, `ts`, and `webm`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A description of the preset (maximum 255 characters)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the preset. (maximum 40 characters)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>thumbnails</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetthumbnails">Dict[Preset<wbr>Thumbnails]</a></span>
    </dt>
    <dd>{{% md %}}Thumbnail parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>video</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideo">Dict[Preset<wbr>Video]</a></span>
    </dt>
    <dd>{{% md %}}Video parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>video_<wbr>codec_<wbr>options</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>video_<wbr>watermarks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideowatermark">List[Preset<wbr>Video<wbr>Watermark]</a></span>
    </dt>
    <dd>{{% md %}}Watermark parameters for the video parameters (documented below)
* `video_codec_options` (Optional, Forces new resource) Codec options for the video parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## Preset Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Audio</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudio">Preset<wbr>Audio?</a></span>
    </dt>
    <dd>{{% md %}}Audio parameters object (documented below).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Audio<wbr>Codec<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudiocodecoptions">Preset<wbr>Audio<wbr>Codec<wbr>Options?</a></span>
    </dt>
    <dd>{{% md %}}Codec options for the audio parameters (documented below)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Container</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The container type for the output file. Valid values are `flac`, `flv`, `fmp4`, `gif`, `mp3`, `mp4`, `mpg`, `mxf`, `oga`, `ogg`, `ts`, and `webm`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A description of the preset (maximum 255 characters)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the preset. (maximum 40 characters)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Thumbnails</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetthumbnails">Preset<wbr>Thumbnails?</a></span>
    </dt>
    <dd>{{% md %}}Thumbnail parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Video</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideo">Preset<wbr>Video?</a></span>
    </dt>
    <dd>{{% md %}}Video parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Video<wbr>Codec<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Video<wbr>Watermarks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideowatermark">List&lt;Preset<wbr>Video<wbr>Watermark&gt;?</a></span>
    </dt>
    <dd>{{% md %}}Watermark parameters for the video parameters (documented below)
* `video_codec_options` (Optional, Forces new resource) Codec options for the video parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Audio</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudio">*Preset<wbr>Audio</a></span>
    </dt>
    <dd>{{% md %}}Audio parameters object (documented below).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Audio<wbr>Codec<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudiocodecoptions">*Preset<wbr>Audio<wbr>Codec<wbr>Options</a></span>
    </dt>
    <dd>{{% md %}}Codec options for the audio parameters (documented below)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Container</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The container type for the output file. Valid values are `flac`, `flv`, `fmp4`, `gif`, `mp3`, `mp4`, `mpg`, `mxf`, `oga`, `ogg`, `ts`, and `webm`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A description of the preset (maximum 255 characters)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the preset. (maximum 40 characters)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Thumbnails</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetthumbnails">*Preset<wbr>Thumbnails</a></span>
    </dt>
    <dd>{{% md %}}Thumbnail parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Video</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideo">*Preset<wbr>Video</a></span>
    </dt>
    <dd>{{% md %}}Video parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Video<wbr>Codec<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Video<wbr>Watermarks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideowatermark">[]Preset<wbr>Video<wbr>Watermark</a></span>
    </dt>
    <dd>{{% md %}}Watermark parameters for the video parameters (documented below)
* `video_codec_options` (Optional, Forces new resource) Codec options for the video parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>audio</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudio">Preset<wbr>Audio?</a></span>
    </dt>
    <dd>{{% md %}}Audio parameters object (documented below).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>audio<wbr>Codec<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudiocodecoptions">Preset<wbr>Audio<wbr>Codec<wbr>Options?</a></span>
    </dt>
    <dd>{{% md %}}Codec options for the audio parameters (documented below)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>container</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The container type for the output file. Valid values are `flac`, `flv`, `fmp4`, `gif`, `mp3`, `mp4`, `mpg`, `mxf`, `oga`, `ogg`, `ts`, and `webm`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A description of the preset (maximum 255 characters)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the preset. (maximum 40 characters)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>thumbnails</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetthumbnails">Preset<wbr>Thumbnails?</a></span>
    </dt>
    <dd>{{% md %}}Thumbnail parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>video</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideo">Preset<wbr>Video?</a></span>
    </dt>
    <dd>{{% md %}}Video parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>video<wbr>Codec<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>video<wbr>Watermarks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideowatermark">Preset<wbr>Video<wbr>Watermark[]?</a></span>
    </dt>
    <dd>{{% md %}}Watermark parameters for the video parameters (documented below)
* `video_codec_options` (Optional, Forces new resource) Codec options for the video parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>audio</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudio">Dict[Preset<wbr>Audio]</a></span>
    </dt>
    <dd>{{% md %}}Audio parameters object (documented below).
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>audio_<wbr>codec_<wbr>options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudiocodecoptions">Dict[Preset<wbr>Audio<wbr>Codec<wbr>Options]</a></span>
    </dt>
    <dd>{{% md %}}Codec options for the audio parameters (documented below)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>container</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The container type for the output file. Valid values are `flac`, `flv`, `fmp4`, `gif`, `mp3`, `mp4`, `mpg`, `mxf`, `oga`, `ogg`, `ts`, and `webm`.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A description of the preset (maximum 255 characters)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the preset. (maximum 40 characters)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>thumbnails</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetthumbnails">Dict[Preset<wbr>Thumbnails]</a></span>
    </dt>
    <dd>{{% md %}}Thumbnail parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>video</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideo">Dict[Preset<wbr>Video]</a></span>
    </dt>
    <dd>{{% md %}}Video parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>video_<wbr>codec_<wbr>options</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>video_<wbr>watermarks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideowatermark">List[Preset<wbr>Video<wbr>Watermark]</a></span>
    </dt>
    <dd>{{% md %}}Watermark parameters for the video parameters (documented below)
* `video_codec_options` (Optional, Forces new resource) Codec options for the video parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing Preset Resource

Get an existing Preset resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/elastictranscoder/#PresetState">PresetState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/aws/elastictranscoder/#Preset">Preset</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>arn=None<span class="p">, </span>audio=None<span class="p">, </span>audio_codec_options=None<span class="p">, </span>container=None<span class="p">, </span>description=None<span class="p">, </span>name=None<span class="p">, </span>thumbnails=None<span class="p">, </span>type=None<span class="p">, </span>video=None<span class="p">, </span>video_codec_options=None<span class="p">, </span>video_watermarks=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetPreset<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/elastictranscoder?tab=doc#PresetState">PresetState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/elastictranscoder?tab=doc#Preset">Preset</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Elastictranscoder.Preset.html">Preset</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Aws/Pulumi.Aws.Elastictranscoder.PresetState.html">PresetState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Audio</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudio">Preset<wbr>Audio<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Audio parameters object (documented below).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Audio<wbr>Codec<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudiocodecoptions">Preset<wbr>Audio<wbr>Codec<wbr>Options<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Codec options for the audio parameters (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Container</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The container type for the output file. Valid values are `flac`, `flv`, `fmp4`, `gif`, `mp3`, `mp4`, `mpg`, `mxf`, `oga`, `ogg`, `ts`, and `webm`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A description of the preset (maximum 255 characters)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the preset. (maximum 40 characters)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Thumbnails</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetthumbnails">Preset<wbr>Thumbnails<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Thumbnail parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Video</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideo">Preset<wbr>Video<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}Video parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Video<wbr>Codec<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary<string, object>?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Video<wbr>Watermarks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideowatermark">List&lt;Preset<wbr>Video<wbr>Watermark<wbr>Args&gt;?</a></span>
    </dt>
    <dd>{{% md %}}Watermark parameters for the video parameters (documented below)
* `video_codec_options` (Optional, Forces new resource) Codec options for the video parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Audio</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudio">*Preset<wbr>Audio</a></span>
    </dt>
    <dd>{{% md %}}Audio parameters object (documented below).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Audio<wbr>Codec<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudiocodecoptions">*Preset<wbr>Audio<wbr>Codec<wbr>Options</a></span>
    </dt>
    <dd>{{% md %}}Codec options for the audio parameters (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Container</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The container type for the output file. Valid values are `flac`, `flv`, `fmp4`, `gif`, `mp3`, `mp4`, `mpg`, `mxf`, `oga`, `ogg`, `ts`, and `webm`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A description of the preset (maximum 255 characters)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The name of the preset. (maximum 40 characters)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Thumbnails</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetthumbnails">*Preset<wbr>Thumbnails</a></span>
    </dt>
    <dd>{{% md %}}Thumbnail parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Video</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideo">*Preset<wbr>Video</a></span>
    </dt>
    <dd>{{% md %}}Video parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Video<wbr>Codec<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Video<wbr>Watermarks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideowatermark">[]Preset<wbr>Video<wbr>Watermark</a></span>
    </dt>
    <dd>{{% md %}}Watermark parameters for the video parameters (documented below)
* `video_codec_options` (Optional, Forces new resource) Codec options for the video parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>audio</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudio">Preset<wbr>Audio?</a></span>
    </dt>
    <dd>{{% md %}}Audio parameters object (documented below).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>audio<wbr>Codec<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudiocodecoptions">Preset<wbr>Audio<wbr>Codec<wbr>Options?</a></span>
    </dt>
    <dd>{{% md %}}Codec options for the audio parameters (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>container</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The container type for the output file. Valid values are `flac`, `flv`, `fmp4`, `gif`, `mp3`, `mp4`, `mpg`, `mxf`, `oga`, `ogg`, `ts`, and `webm`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A description of the preset (maximum 255 characters)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The name of the preset. (maximum 40 characters)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>thumbnails</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetthumbnails">Preset<wbr>Thumbnails?</a></span>
    </dt>
    <dd>{{% md %}}Thumbnail parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>video</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideo">Preset<wbr>Video?</a></span>
    </dt>
    <dd>{{% md %}}Video parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>video<wbr>Codec<wbr>Options</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>video<wbr>Watermarks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideowatermark">Preset<wbr>Video<wbr>Watermark[]?</a></span>
    </dt>
    <dd>{{% md %}}Watermark parameters for the video parameters (documented below)
* `video_codec_options` (Optional, Forces new resource) Codec options for the video parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>arn</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>audio</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudio">Dict[Preset<wbr>Audio]</a></span>
    </dt>
    <dd>{{% md %}}Audio parameters object (documented below).
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>audio_<wbr>codec_<wbr>options</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetaudiocodecoptions">Dict[Preset<wbr>Audio<wbr>Codec<wbr>Options]</a></span>
    </dt>
    <dd>{{% md %}}Codec options for the audio parameters (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>container</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The container type for the output file. Valid values are `flac`, `flv`, `fmp4`, `gif`, `mp3`, `mp4`, `mpg`, `mxf`, `oga`, `ogg`, `ts`, and `webm`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A description of the preset (maximum 255 characters)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the preset. (maximum 40 characters)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>thumbnails</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetthumbnails">Dict[Preset<wbr>Thumbnails]</a></span>
    </dt>
    <dd>{{% md %}}Thumbnail parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>video</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideo">Dict[Preset<wbr>Video]</a></span>
    </dt>
    <dd>{{% md %}}Video parameters object (documented below)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>video_<wbr>codec_<wbr>options</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dict[str, Any]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>video_<wbr>watermarks</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#presetvideowatermark">List[Preset<wbr>Video<wbr>Watermark]</a></span>
    </dt>
    <dd>{{% md %}}Watermark parameters for the video parameters (documented below)
* `video_codec_options` (Optional, Forces new resource) Codec options for the video parameters
{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Preset<wbr>Audio</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#PresetAudio">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#PresetAudio">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/elastictranscoder?tab=doc#PresetAudioArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/elastictranscoder?tab=doc#PresetAudioOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Audio<wbr>Packing<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The method of organizing audio channels and tracks. Use Audio:Channels to specify the number of channels in your output, and Audio:AudioPackingMode to specify the number of tracks and their relation to the channels. If you do not specify an Audio:AudioPackingMode, Elastic Transcoder uses SingleTrack.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Bit<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The bit rate of the audio stream in the output file, in kilobits/second. Enter an integer between 64 and 320, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Channels</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The number of audio channels in the output file
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Codec</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The audio codec for the output file. Valid values are `AAC`, `flac`, `mp2`, `mp3`, `pcm`, and `vorbis`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sample<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The sample rate of the audio stream in the output file, in hertz. Valid values are: `auto`, `22050`, `32000`, `44100`, `48000`, `96000`
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Audio<wbr>Packing<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The method of organizing audio channels and tracks. Use Audio:Channels to specify the number of channels in your output, and Audio:AudioPackingMode to specify the number of tracks and their relation to the channels. If you do not specify an Audio:AudioPackingMode, Elastic Transcoder uses SingleTrack.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Bit<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The bit rate of the audio stream in the output file, in kilobits/second. Enter an integer between 64 and 320, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Channels</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The number of audio channels in the output file
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Codec</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The audio codec for the output file. Valid values are `AAC`, `flac`, `mp2`, `mp3`, `pcm`, and `vorbis`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sample<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The sample rate of the audio stream in the output file, in hertz. Valid values are: `auto`, `22050`, `32000`, `44100`, `48000`, `96000`
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>audio<wbr>Packing<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The method of organizing audio channels and tracks. Use Audio:Channels to specify the number of channels in your output, and Audio:AudioPackingMode to specify the number of tracks and their relation to the channels. If you do not specify an Audio:AudioPackingMode, Elastic Transcoder uses SingleTrack.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>bit<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The bit rate of the audio stream in the output file, in kilobits/second. Enter an integer between 64 and 320, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>channels</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The number of audio channels in the output file
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>codec</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The audio codec for the output file. Valid values are `AAC`, `flac`, `mp2`, `mp3`, `pcm`, and `vorbis`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sample<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The sample rate of the audio stream in the output file, in hertz. Valid values are: `auto`, `22050`, `32000`, `44100`, `48000`, `96000`
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>audio<wbr>Packing<wbr>Mode</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The method of organizing audio channels and tracks. Use Audio:Channels to specify the number of channels in your output, and Audio:AudioPackingMode to specify the number of tracks and their relation to the channels. If you do not specify an Audio:AudioPackingMode, Elastic Transcoder uses SingleTrack.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>bit<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The bit rate of the audio stream in the output file, in kilobits/second. Enter an integer between 64 and 320, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>channels</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The number of audio channels in the output file
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>codec</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The audio codec for the output file. Valid values are `AAC`, `flac`, `mp2`, `mp3`, `pcm`, and `vorbis`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sample<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The sample rate of the audio stream in the output file, in hertz. Valid values are: `auto`, `22050`, `32000`, `44100`, `48000`, `96000`
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Preset<wbr>Audio<wbr>Codec<wbr>Options</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#PresetAudioCodecOptions">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#PresetAudioCodecOptions">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/elastictranscoder?tab=doc#PresetAudioCodecOptionsArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/elastictranscoder?tab=doc#PresetAudioCodecOptionsOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Bit<wbr>Depth</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The bit depth of a sample is how many bits of information are included in the audio samples. Valid values are `16` and `24`. (FLAC/PCM Only)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Bit<wbr>Order</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The order the bits of a PCM sample are stored in. The supported value is LittleEndian. (PCM Only)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Profile</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}If you specified AAC for Audio:Codec, choose the AAC profile for the output file.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Signed</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Whether audio samples are represented with negative and positive numbers (signed) or only positive numbers (unsigned). The supported value is Signed. (PCM Only)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Bit<wbr>Depth</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The bit depth of a sample is how many bits of information are included in the audio samples. Valid values are `16` and `24`. (FLAC/PCM Only)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Bit<wbr>Order</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The order the bits of a PCM sample are stored in. The supported value is LittleEndian. (PCM Only)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Profile</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}If you specified AAC for Audio:Codec, choose the AAC profile for the output file.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Signed</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Whether audio samples are represented with negative and positive numbers (signed) or only positive numbers (unsigned). The supported value is Signed. (PCM Only)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>bit<wbr>Depth</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The bit depth of a sample is how many bits of information are included in the audio samples. Valid values are `16` and `24`. (FLAC/PCM Only)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>bit<wbr>Order</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The order the bits of a PCM sample are stored in. The supported value is LittleEndian. (PCM Only)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>profile</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}If you specified AAC for Audio:Codec, choose the AAC profile for the output file.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>signed</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Whether audio samples are represented with negative and positive numbers (signed) or only positive numbers (unsigned). The supported value is Signed. (PCM Only)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>bit<wbr>Depth</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The bit depth of a sample is how many bits of information are included in the audio samples. Valid values are `16` and `24`. (FLAC/PCM Only)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>bit<wbr>Order</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The order the bits of a PCM sample are stored in. The supported value is LittleEndian. (PCM Only)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>profile</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}If you specified AAC for Audio:Codec, choose the AAC profile for the output file.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>signed</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Whether audio samples are represented with negative and positive numbers (signed) or only positive numbers (unsigned). The supported value is Signed. (PCM Only)
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Preset<wbr>Thumbnails</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#PresetThumbnails">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#PresetThumbnails">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/elastictranscoder?tab=doc#PresetThumbnailsArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/elastictranscoder?tab=doc#PresetThumbnailsOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Aspect<wbr>Ratio</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The aspect ratio of thumbnails. The following values are valid: auto, 1:1, 4:3, 3:2, 16:9
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Format</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The format of thumbnails, if any. Valid formats are jpg and png.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Interval</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The approximate number of seconds between thumbnails. The value must be an integer. The actual interval can vary by several seconds from one thumbnail to the next.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Height</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The maximum height of thumbnails, in pixels. If you specify auto, Elastic Transcoder uses 1080 (Full HD) as the default value. If you specify a numeric value, enter an even integer between 32 and 3072, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Width</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The maximum width of thumbnails, in pixels. If you specify auto, Elastic Transcoder uses 1920 (Full HD) as the default value. If you specify a numeric value, enter an even integer between 32 and 4096, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Padding<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}When you set PaddingPolicy to Pad, Elastic Transcoder might add black bars to the top and bottom and/or left and right sides of thumbnails to make the total size of the thumbnails match the values that you specified for thumbnail MaxWidth and MaxHeight settings.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Resolution</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The width and height of thumbnail files in pixels, in the format WidthxHeight, where both values are even integers. The values cannot exceed the width and height that you specified in the Video:Resolution object. (To better control resolution and aspect ratio of thumbnails, we recommend that you use the thumbnail values `max_width`, `max_height`, `sizing_policy`, and `padding_policy` instead of `resolution` and `aspect_ratio`. The two groups of settings are mutually exclusive. Do not use them together)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sizing<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A value that controls scaling of thumbnails. Valid values are: `Fit`, `Fill`, `Stretch`, `Keep`, `ShrinkToFit`, and `ShrinkToFill`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Aspect<wbr>Ratio</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The aspect ratio of thumbnails. The following values are valid: auto, 1:1, 4:3, 3:2, 16:9
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Format</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The format of thumbnails, if any. Valid formats are jpg and png.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Interval</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The approximate number of seconds between thumbnails. The value must be an integer. The actual interval can vary by several seconds from one thumbnail to the next.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Height</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The maximum height of thumbnails, in pixels. If you specify auto, Elastic Transcoder uses 1080 (Full HD) as the default value. If you specify a numeric value, enter an even integer between 32 and 3072, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Width</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The maximum width of thumbnails, in pixels. If you specify auto, Elastic Transcoder uses 1920 (Full HD) as the default value. If you specify a numeric value, enter an even integer between 32 and 4096, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Padding<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}When you set PaddingPolicy to Pad, Elastic Transcoder might add black bars to the top and bottom and/or left and right sides of thumbnails to make the total size of the thumbnails match the values that you specified for thumbnail MaxWidth and MaxHeight settings.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Resolution</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The width and height of thumbnail files in pixels, in the format WidthxHeight, where both values are even integers. The values cannot exceed the width and height that you specified in the Video:Resolution object. (To better control resolution and aspect ratio of thumbnails, we recommend that you use the thumbnail values `max_width`, `max_height`, `sizing_policy`, and `padding_policy` instead of `resolution` and `aspect_ratio`. The two groups of settings are mutually exclusive. Do not use them together)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sizing<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A value that controls scaling of thumbnails. Valid values are: `Fit`, `Fill`, `Stretch`, `Keep`, `ShrinkToFit`, and `ShrinkToFill`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>aspect<wbr>Ratio</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The aspect ratio of thumbnails. The following values are valid: auto, 1:1, 4:3, 3:2, 16:9
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>format</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The format of thumbnails, if any. Valid formats are jpg and png.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>interval</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The approximate number of seconds between thumbnails. The value must be an integer. The actual interval can vary by several seconds from one thumbnail to the next.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Height</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The maximum height of thumbnails, in pixels. If you specify auto, Elastic Transcoder uses 1080 (Full HD) as the default value. If you specify a numeric value, enter an even integer between 32 and 3072, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Width</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The maximum width of thumbnails, in pixels. If you specify auto, Elastic Transcoder uses 1920 (Full HD) as the default value. If you specify a numeric value, enter an even integer between 32 and 4096, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>padding<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}When you set PaddingPolicy to Pad, Elastic Transcoder might add black bars to the top and bottom and/or left and right sides of thumbnails to make the total size of the thumbnails match the values that you specified for thumbnail MaxWidth and MaxHeight settings.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>resolution</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The width and height of thumbnail files in pixels, in the format WidthxHeight, where both values are even integers. The values cannot exceed the width and height that you specified in the Video:Resolution object. (To better control resolution and aspect ratio of thumbnails, we recommend that you use the thumbnail values `max_width`, `max_height`, `sizing_policy`, and `padding_policy` instead of `resolution` and `aspect_ratio`. The two groups of settings are mutually exclusive. Do not use them together)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sizing<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A value that controls scaling of thumbnails. Valid values are: `Fit`, `Fill`, `Stretch`, `Keep`, `ShrinkToFit`, and `ShrinkToFill`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>aspect<wbr>Ratio</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The aspect ratio of thumbnails. The following values are valid: auto, 1:1, 4:3, 3:2, 16:9
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>format</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The format of thumbnails, if any. Valid formats are jpg and png.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>interval</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The approximate number of seconds between thumbnails. The value must be an integer. The actual interval can vary by several seconds from one thumbnail to the next.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Height</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The maximum height of thumbnails, in pixels. If you specify auto, Elastic Transcoder uses 1080 (Full HD) as the default value. If you specify a numeric value, enter an even integer between 32 and 3072, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Width</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The maximum width of thumbnails, in pixels. If you specify auto, Elastic Transcoder uses 1920 (Full HD) as the default value. If you specify a numeric value, enter an even integer between 32 and 4096, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>padding<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}When you set PaddingPolicy to Pad, Elastic Transcoder might add black bars to the top and bottom and/or left and right sides of thumbnails to make the total size of the thumbnails match the values that you specified for thumbnail MaxWidth and MaxHeight settings.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>resolution</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The width and height of thumbnail files in pixels, in the format WidthxHeight, where both values are even integers. The values cannot exceed the width and height that you specified in the Video:Resolution object. (To better control resolution and aspect ratio of thumbnails, we recommend that you use the thumbnail values `max_width`, `max_height`, `sizing_policy`, and `padding_policy` instead of `resolution` and `aspect_ratio`. The two groups of settings are mutually exclusive. Do not use them together)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sizing<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A value that controls scaling of thumbnails. Valid values are: `Fit`, `Fill`, `Stretch`, `Keep`, `ShrinkToFit`, and `ShrinkToFill`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Preset<wbr>Video</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#PresetVideo">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#PresetVideo">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/elastictranscoder?tab=doc#PresetVideoArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/elastictranscoder?tab=doc#PresetVideoOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Aspect<wbr>Ratio</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The display aspect ratio of the video in the output file. Valid values are: `auto`, `1:1`, `4:3`, `3:2`, `16:9`. (Note; to better control resolution and aspect ratio of output videos, we recommend that you use the values `max_width`, `max_height`, `sizing_policy`, `padding_policy`, and `display_aspect_ratio` instead of `resolution` and `aspect_ratio`.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Bit<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The bit rate of the video stream in the output file, in kilobits/second. You can configure variable bit rate or constant bit rate encoding.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Codec</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The video codec for the output file. Valid values are `gif`, `H.264`, `mpeg2`, `vp8`, and `vp9`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Display<wbr>Aspect<wbr>Ratio</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The value that Elastic Transcoder adds to the metadata in the output file. If you set DisplayAspectRatio to auto, Elastic Transcoder chooses an aspect ratio that ensures square pixels. If you specify another option, Elastic Transcoder sets that value in the output file.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fixed<wbr>Gop</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Whether to use a fixed value for Video:FixedGOP. Not applicable for containers of type gif. Valid values are true and false. Also known as, Fixed Number of Frames Between Keyframes.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Frame<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The frames per second for the video stream in the output file. The following values are valid: `auto`, `10`, `15`, `23.97`, `24`, `25`, `29.97`, `30`, `50`, `60`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Keyframes<wbr>Max<wbr>Dist</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The maximum number of frames between key frames. Not applicable for containers of type gif.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Frame<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}If you specify auto for FrameRate, Elastic Transcoder uses the frame rate of the input video for the frame rate of the output video, up to the maximum frame rate. If you do not specify a MaxFrameRate, Elastic Transcoder will use a default of 30.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Height</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The maximum height of the output video in pixels. If you specify auto, Elastic Transcoder uses 1080 (Full HD) as the default value. If you specify a numeric value, enter an even integer between 96 and 3072, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Width</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The maximum width of the output video in pixels. If you specify auto, Elastic Transcoder uses 1920 (Full HD) as the default value. If you specify a numeric value, enter an even integer between 128 and 4096, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Padding<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}When you set PaddingPolicy to Pad, Elastic Transcoder might add black bars to the top and bottom and/or left and right sides of the output video to make the total size of the output video match the values that you specified for `max_width` and `max_height`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Resolution</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The width and height of the video in the output file, in pixels. Valid values are `auto` and `widthxheight`. (see note for `aspect_ratio`)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sizing<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A value that controls scaling of the output video. Valid values are: `Fit`, `Fill`, `Stretch`, `Keep`, `ShrinkToFit`, `ShrinkToFill`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Aspect<wbr>Ratio</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The display aspect ratio of the video in the output file. Valid values are: `auto`, `1:1`, `4:3`, `3:2`, `16:9`. (Note; to better control resolution and aspect ratio of output videos, we recommend that you use the values `max_width`, `max_height`, `sizing_policy`, `padding_policy`, and `display_aspect_ratio` instead of `resolution` and `aspect_ratio`.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Bit<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The bit rate of the video stream in the output file, in kilobits/second. You can configure variable bit rate or constant bit rate encoding.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Codec</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The video codec for the output file. Valid values are `gif`, `H.264`, `mpeg2`, `vp8`, and `vp9`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Display<wbr>Aspect<wbr>Ratio</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The value that Elastic Transcoder adds to the metadata in the output file. If you set DisplayAspectRatio to auto, Elastic Transcoder chooses an aspect ratio that ensures square pixels. If you specify another option, Elastic Transcoder sets that value in the output file.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fixed<wbr>Gop</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Whether to use a fixed value for Video:FixedGOP. Not applicable for containers of type gif. Valid values are true and false. Also known as, Fixed Number of Frames Between Keyframes.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Frame<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The frames per second for the video stream in the output file. The following values are valid: `auto`, `10`, `15`, `23.97`, `24`, `25`, `29.97`, `30`, `50`, `60`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Keyframes<wbr>Max<wbr>Dist</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The maximum number of frames between key frames. Not applicable for containers of type gif.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Frame<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}If you specify auto for FrameRate, Elastic Transcoder uses the frame rate of the input video for the frame rate of the output video, up to the maximum frame rate. If you do not specify a MaxFrameRate, Elastic Transcoder will use a default of 30.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Height</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The maximum height of the output video in pixels. If you specify auto, Elastic Transcoder uses 1080 (Full HD) as the default value. If you specify a numeric value, enter an even integer between 96 and 3072, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Width</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The maximum width of the output video in pixels. If you specify auto, Elastic Transcoder uses 1920 (Full HD) as the default value. If you specify a numeric value, enter an even integer between 128 and 4096, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Padding<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}When you set PaddingPolicy to Pad, Elastic Transcoder might add black bars to the top and bottom and/or left and right sides of the output video to make the total size of the output video match the values that you specified for `max_width` and `max_height`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Resolution</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The width and height of the video in the output file, in pixels. Valid values are `auto` and `widthxheight`. (see note for `aspect_ratio`)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sizing<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A value that controls scaling of the output video. Valid values are: `Fit`, `Fill`, `Stretch`, `Keep`, `ShrinkToFit`, `ShrinkToFill`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>aspect<wbr>Ratio</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The display aspect ratio of the video in the output file. Valid values are: `auto`, `1:1`, `4:3`, `3:2`, `16:9`. (Note; to better control resolution and aspect ratio of output videos, we recommend that you use the values `max_width`, `max_height`, `sizing_policy`, `padding_policy`, and `display_aspect_ratio` instead of `resolution` and `aspect_ratio`.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>bit<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The bit rate of the video stream in the output file, in kilobits/second. You can configure variable bit rate or constant bit rate encoding.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>codec</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The video codec for the output file. Valid values are `gif`, `H.264`, `mpeg2`, `vp8`, and `vp9`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>display<wbr>Aspect<wbr>Ratio</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The value that Elastic Transcoder adds to the metadata in the output file. If you set DisplayAspectRatio to auto, Elastic Transcoder chooses an aspect ratio that ensures square pixels. If you specify another option, Elastic Transcoder sets that value in the output file.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fixed<wbr>Gop</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Whether to use a fixed value for Video:FixedGOP. Not applicable for containers of type gif. Valid values are true and false. Also known as, Fixed Number of Frames Between Keyframes.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>frame<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The frames per second for the video stream in the output file. The following values are valid: `auto`, `10`, `15`, `23.97`, `24`, `25`, `29.97`, `30`, `50`, `60`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>keyframes<wbr>Max<wbr>Dist</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The maximum number of frames between key frames. Not applicable for containers of type gif.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Frame<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}If you specify auto for FrameRate, Elastic Transcoder uses the frame rate of the input video for the frame rate of the output video, up to the maximum frame rate. If you do not specify a MaxFrameRate, Elastic Transcoder will use a default of 30.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Height</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The maximum height of the output video in pixels. If you specify auto, Elastic Transcoder uses 1080 (Full HD) as the default value. If you specify a numeric value, enter an even integer between 96 and 3072, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Width</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The maximum width of the output video in pixels. If you specify auto, Elastic Transcoder uses 1920 (Full HD) as the default value. If you specify a numeric value, enter an even integer between 128 and 4096, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>padding<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}When you set PaddingPolicy to Pad, Elastic Transcoder might add black bars to the top and bottom and/or left and right sides of the output video to make the total size of the output video match the values that you specified for `max_width` and `max_height`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>resolution</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The width and height of the video in the output file, in pixels. Valid values are `auto` and `widthxheight`. (see note for `aspect_ratio`)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sizing<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A value that controls scaling of the output video. Valid values are: `Fit`, `Fill`, `Stretch`, `Keep`, `ShrinkToFit`, `ShrinkToFill`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>aspect<wbr>Ratio</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The display aspect ratio of the video in the output file. Valid values are: `auto`, `1:1`, `4:3`, `3:2`, `16:9`. (Note; to better control resolution and aspect ratio of output videos, we recommend that you use the values `max_width`, `max_height`, `sizing_policy`, `padding_policy`, and `display_aspect_ratio` instead of `resolution` and `aspect_ratio`.)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>bit<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The bit rate of the video stream in the output file, in kilobits/second. You can configure variable bit rate or constant bit rate encoding.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>codec</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The video codec for the output file. Valid values are `gif`, `H.264`, `mpeg2`, `vp8`, and `vp9`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>display<wbr>Aspect<wbr>Ratio</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The value that Elastic Transcoder adds to the metadata in the output file. If you set DisplayAspectRatio to auto, Elastic Transcoder chooses an aspect ratio that ensures square pixels. If you specify another option, Elastic Transcoder sets that value in the output file.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fixed<wbr>Gop</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Whether to use a fixed value for Video:FixedGOP. Not applicable for containers of type gif. Valid values are true and false. Also known as, Fixed Number of Frames Between Keyframes.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>frame<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The frames per second for the video stream in the output file. The following values are valid: `auto`, `10`, `15`, `23.97`, `24`, `25`, `29.97`, `30`, `50`, `60`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>keyframes<wbr>Max<wbr>Dist</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The maximum number of frames between key frames. Not applicable for containers of type gif.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Frame<wbr>Rate</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}If you specify auto for FrameRate, Elastic Transcoder uses the frame rate of the input video for the frame rate of the output video, up to the maximum frame rate. If you do not specify a MaxFrameRate, Elastic Transcoder will use a default of 30.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Height</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The maximum height of the output video in pixels. If you specify auto, Elastic Transcoder uses 1080 (Full HD) as the default value. If you specify a numeric value, enter an even integer between 96 and 3072, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Width</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The maximum width of the output video in pixels. If you specify auto, Elastic Transcoder uses 1920 (Full HD) as the default value. If you specify a numeric value, enter an even integer between 128 and 4096, inclusive.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>padding<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}When you set PaddingPolicy to Pad, Elastic Transcoder might add black bars to the top and bottom and/or left and right sides of the output video to make the total size of the output video match the values that you specified for `max_width` and `max_height`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>resolution</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The width and height of the video in the output file, in pixels. Valid values are `auto` and `widthxheight`. (see note for `aspect_ratio`)
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sizing<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A value that controls scaling of the output video. Valid values are: `Fit`, `Fill`, `Stretch`, `Keep`, `ShrinkToFit`, `ShrinkToFill`.
{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Preset<wbr>Video<wbr>Watermark</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/input/#PresetVideoWatermark">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/aws/types/output/#PresetVideoWatermark">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/elastictranscoder?tab=doc#PresetVideoWatermarkArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-aws/sdk/go/aws/elastictranscoder?tab=doc#PresetVideoWatermarkOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Horizontal<wbr>Align</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The horizontal position of the watermark unless you specify a nonzero value for `horzontal_offset`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Horizontal<wbr>Offset</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The amount by which you want the horizontal position of the watermark to be offset from the position specified by `horizontal_align`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A unique identifier for the settings for one watermark. The value of Id can be up to 40 characters long. You can specify settings for up to four watermarks.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Height</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The maximum height of the watermark.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Width</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The maximum width of the watermark.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Opacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A percentage that indicates how much you want a watermark to obscure the video in the location where it appears.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sizing<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A value that controls scaling of the watermark. Valid values are: `Fit`, `Stretch`, `ShrinkToFit`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A value that determines how Elastic Transcoder interprets values that you specified for `video_watermarks.horizontal_offset`, `video_watermarks.vertical_offset`, `video_watermarks.max_width`, and `video_watermarks.max_height`. Valid values are `Content` and `Frame`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vertical<wbr>Align</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The vertical position of the watermark unless you specify a nonzero value for `vertical_align`. Valid values are `Top`, `Bottom`, `Center`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vertical<wbr>Offset</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The amount by which you want the vertical position of the watermark to be offset from the position specified by `vertical_align`
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Horizontal<wbr>Align</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The horizontal position of the watermark unless you specify a nonzero value for `horzontal_offset`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Horizontal<wbr>Offset</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The amount by which you want the horizontal position of the watermark to be offset from the position specified by `horizontal_align`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Id</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A unique identifier for the settings for one watermark. The value of Id can be up to 40 characters long. You can specify settings for up to four watermarks.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Height</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The maximum height of the watermark.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Max<wbr>Width</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The maximum width of the watermark.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Opacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A percentage that indicates how much you want a watermark to obscure the video in the location where it appears.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Sizing<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A value that controls scaling of the watermark. Valid values are: `Fit`, `Stretch`, `ShrinkToFit`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Target</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}A value that determines how Elastic Transcoder interprets values that you specified for `video_watermarks.horizontal_offset`, `video_watermarks.vertical_offset`, `video_watermarks.max_width`, and `video_watermarks.max_height`. Valid values are `Content` and `Frame`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vertical<wbr>Align</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The vertical position of the watermark unless you specify a nonzero value for `vertical_align`. Valid values are `Top`, `Bottom`, `Center`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Vertical<wbr>Offset</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}The amount by which you want the vertical position of the watermark to be offset from the position specified by `vertical_align`
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>horizontal<wbr>Align</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The horizontal position of the watermark unless you specify a nonzero value for `horzontal_offset`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>horizontal<wbr>Offset</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The amount by which you want the horizontal position of the watermark to be offset from the position specified by `horizontal_align`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A unique identifier for the settings for one watermark. The value of Id can be up to 40 characters long. You can specify settings for up to four watermarks.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Height</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The maximum height of the watermark.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Width</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The maximum width of the watermark.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>opacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A percentage that indicates how much you want a watermark to obscure the video in the location where it appears.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sizing<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A value that controls scaling of the watermark. Valid values are: `Fit`, `Stretch`, `ShrinkToFit`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}A value that determines how Elastic Transcoder interprets values that you specified for `video_watermarks.horizontal_offset`, `video_watermarks.vertical_offset`, `video_watermarks.max_width`, and `video_watermarks.max_height`. Valid values are `Content` and `Frame`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vertical<wbr>Align</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The vertical position of the watermark unless you specify a nonzero value for `vertical_align`. Valid values are `Top`, `Bottom`, `Center`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vertical<wbr>Offset</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}The amount by which you want the vertical position of the watermark to be offset from the position specified by `vertical_align`
{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>horizontal<wbr>Align</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The horizontal position of the watermark unless you specify a nonzero value for `horzontal_offset`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>horizontal<wbr>Offset</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The amount by which you want the horizontal position of the watermark to be offset from the position specified by `horizontal_align`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A unique identifier for the settings for one watermark. The value of Id can be up to 40 characters long. You can specify settings for up to four watermarks.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Height</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The maximum height of the watermark.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>max<wbr>Width</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The maximum width of the watermark.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>opacity</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A percentage that indicates how much you want a watermark to obscure the video in the location where it appears.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>sizing<wbr>Policy</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A value that controls scaling of the watermark. Valid values are: `Fit`, `Stretch`, `ShrinkToFit`
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>target</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A value that determines how Elastic Transcoder interprets values that you specified for `video_watermarks.horizontal_offset`, `video_watermarks.vertical_offset`, `video_watermarks.max_width`, and `video_watermarks.max_height`. Valid values are `Content` and `Frame`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vertical<wbr>Align</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The vertical position of the watermark unless you specify a nonzero value for `vertical_align`. Valid values are `Top`, `Bottom`, `Center`.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>vertical<wbr>Offset</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The amount by which you want the vertical position of the watermark to be offset from the position specified by `vertical_align`
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

