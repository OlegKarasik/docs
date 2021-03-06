
---
title: "MfaPolicy"
block_external_search_index: true
---






## Create a MfaPolicy Resource

{{< chooser language "javascript,typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/okta/deprecated/#MfaPolicy">MfaPolicy</a></span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">args</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/okta/deprecated/#MfaPolicyArgs">MfaPolicyArgs</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span><span class="nf">MfaPolicy</span><span class="p">(resource_name, opts=None, </span>description=None<span class="p">, </span>duo=None<span class="p">, </span>fido_u2f=None<span class="p">, </span>fido_webauthn=None<span class="p">, </span>google_otp=None<span class="p">, </span>groups_includeds=None<span class="p">, </span>name=None<span class="p">, </span>okta_call=None<span class="p">, </span>okta_otp=None<span class="p">, </span>okta_password=None<span class="p">, </span>okta_push=None<span class="p">, </span>okta_question=None<span class="p">, </span>okta_sms=None<span class="p">, </span>priority=None<span class="p">, </span>rsa_token=None<span class="p">, </span>status=None<span class="p">, </span>symantec_vip=None<span class="p">, </span>yubikey_token=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>NewMfaPolicy<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">pulumi.Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">args</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyArgs">MfaPolicyArgs</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">pulumi.ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicy">MfaPolicy</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Okta/Pulumi.Okta.Deprecated.MfaPolicy.html">MfaPolicy</a></span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Okta/Pulumi.Okta.Deprecated.MfaPolicyArgs.html">MfaPolicyArgs</a></span>? <span class="nx">args = null<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Policy Description
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Duo</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyduo">Mfa<wbr>Policy<wbr>Duo<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fido<wbr>U2f</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidou2f">Mfa<wbr>Policy<wbr>Fido<wbr>U2f<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fido<wbr>Webauthn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidowebauthn">Mfa<wbr>Policy<wbr>Fido<wbr>Webauthn<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Google<wbr>Otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicygoogleotp">Mfa<wbr>Policy<wbr>Google<wbr>Otp<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Groups<wbr>Includeds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}List of Group IDs to Include
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Policy Name
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Call</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktacall">Mfa<wbr>Policy<wbr>Okta<wbr>Call<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaotp">Mfa<wbr>Policy<wbr>Okta<wbr>Otp<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapassword">Mfa<wbr>Policy<wbr>Okta<wbr>Password<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Push</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapush">Mfa<wbr>Policy<wbr>Okta<wbr>Push<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Question</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaquestion">Mfa<wbr>Policy<wbr>Okta<wbr>Question<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Sms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktasms">Mfa<wbr>Policy<wbr>Okta<wbr>Sms<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Policy Priority, this attribute can be set to a valid priority. To avoid endless diff situation we error if an invalid
priority is provided. API defaults it to the last/lowest if not there.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Rsa<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyrsatoken">Mfa<wbr>Policy<wbr>Rsa<wbr>Token<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Policy Status: ACTIVE or INACTIVE.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Symantec<wbr>Vip</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicysymantecvip">Mfa<wbr>Policy<wbr>Symantec<wbr>Vip<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Yubikey<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyyubikeytoken">Mfa<wbr>Policy<wbr>Yubikey<wbr>Token<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Policy Description
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Duo</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyduo">*Mfa<wbr>Policy<wbr>Duo</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fido<wbr>U2f</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidou2f">*Mfa<wbr>Policy<wbr>Fido<wbr>U2f</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fido<wbr>Webauthn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidowebauthn">*Mfa<wbr>Policy<wbr>Fido<wbr>Webauthn</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Google<wbr>Otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicygoogleotp">*Mfa<wbr>Policy<wbr>Google<wbr>Otp</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Groups<wbr>Includeds</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of Group IDs to Include
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Policy Name
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Call</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktacall">*Mfa<wbr>Policy<wbr>Okta<wbr>Call</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaotp">*Mfa<wbr>Policy<wbr>Okta<wbr>Otp</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapassword">*Mfa<wbr>Policy<wbr>Okta<wbr>Password</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Push</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapush">*Mfa<wbr>Policy<wbr>Okta<wbr>Push</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Question</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaquestion">*Mfa<wbr>Policy<wbr>Okta<wbr>Question</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Sms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktasms">*Mfa<wbr>Policy<wbr>Okta<wbr>Sms</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Policy Priority, this attribute can be set to a valid priority. To avoid endless diff situation we error if an invalid
priority is provided. API defaults it to the last/lowest if not there.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Rsa<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyrsatoken">*Mfa<wbr>Policy<wbr>Rsa<wbr>Token</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Policy Status: ACTIVE or INACTIVE.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Symantec<wbr>Vip</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicysymantecvip">*Mfa<wbr>Policy<wbr>Symantec<wbr>Vip</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Yubikey<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyyubikeytoken">*Mfa<wbr>Policy<wbr>Yubikey<wbr>Token</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Policy Description
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>duo</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyduo">Mfa<wbr>Policy<wbr>Duo?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fido<wbr>U2f</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidou2f">Mfa<wbr>Policy<wbr>Fido<wbr>U2f?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fido<wbr>Webauthn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidowebauthn">Mfa<wbr>Policy<wbr>Fido<wbr>Webauthn?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>google<wbr>Otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicygoogleotp">Mfa<wbr>Policy<wbr>Google<wbr>Otp?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>groups<wbr>Includeds</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}List of Group IDs to Include
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Policy Name
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta<wbr>Call</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktacall">Mfa<wbr>Policy<wbr>Okta<wbr>Call?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta<wbr>Otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaotp">Mfa<wbr>Policy<wbr>Okta<wbr>Otp?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapassword">Mfa<wbr>Policy<wbr>Okta<wbr>Password?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta<wbr>Push</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapush">Mfa<wbr>Policy<wbr>Okta<wbr>Push?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta<wbr>Question</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaquestion">Mfa<wbr>Policy<wbr>Okta<wbr>Question?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta<wbr>Sms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktasms">Mfa<wbr>Policy<wbr>Okta<wbr>Sms?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Policy Priority, this attribute can be set to a valid priority. To avoid endless diff situation we error if an invalid
priority is provided. API defaults it to the last/lowest if not there.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>rsa<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyrsatoken">Mfa<wbr>Policy<wbr>Rsa<wbr>Token?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Policy Status: ACTIVE or INACTIVE.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>symantec<wbr>Vip</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicysymantecvip">Mfa<wbr>Policy<wbr>Symantec<wbr>Vip?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>yubikey<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyyubikeytoken">Mfa<wbr>Policy<wbr>Yubikey<wbr>Token?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Policy Description
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>duo</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyduo">Dict[Mfa<wbr>Policy<wbr>Duo]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fido_<wbr>u2f</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidou2f">Dict[Mfa<wbr>Policy<wbr>Fido<wbr>U2f]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fido_<wbr>webauthn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidowebauthn">Dict[Mfa<wbr>Policy<wbr>Fido<wbr>Webauthn]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>google_<wbr>otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicygoogleotp">Dict[Mfa<wbr>Policy<wbr>Google<wbr>Otp]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>groups_<wbr>includeds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}List of Group IDs to Include
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Policy Name
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta_<wbr>call</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktacall">Dict[Mfa<wbr>Policy<wbr>Okta<wbr>Call]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta_<wbr>otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaotp">Dict[Mfa<wbr>Policy<wbr>Okta<wbr>Otp]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta_<wbr>password</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapassword">Dict[Mfa<wbr>Policy<wbr>Okta<wbr>Password]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta_<wbr>push</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapush">Dict[Mfa<wbr>Policy<wbr>Okta<wbr>Push]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta_<wbr>question</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaquestion">Dict[Mfa<wbr>Policy<wbr>Okta<wbr>Question]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta_<wbr>sms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktasms">Dict[Mfa<wbr>Policy<wbr>Okta<wbr>Sms]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Policy Priority, this attribute can be set to a valid priority. To avoid endless diff situation we error if an invalid
priority is provided. API defaults it to the last/lowest if not there.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>rsa_<wbr>token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyrsatoken">Dict[Mfa<wbr>Policy<wbr>Rsa<wbr>Token]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Policy Status: ACTIVE or INACTIVE.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>symantec_<wbr>vip</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicysymantecvip">Dict[Mfa<wbr>Policy<wbr>Symantec<wbr>Vip]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>yubikey_<wbr>token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyyubikeytoken">Dict[Mfa<wbr>Policy<wbr>Yubikey<wbr>Token]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}







## MfaPolicy Output Properties

The following output properties are available:




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Policy Description
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Duo</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyduo">Mfa<wbr>Policy<wbr>Duo?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Fido<wbr>U2f</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidou2f">Mfa<wbr>Policy<wbr>Fido<wbr>U2f?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Fido<wbr>Webauthn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidowebauthn">Mfa<wbr>Policy<wbr>Fido<wbr>Webauthn?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Google<wbr>Otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicygoogleotp">Mfa<wbr>Policy<wbr>Google<wbr>Otp?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Groups<wbr>Includeds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}List of Group IDs to Include
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Policy Name
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Okta<wbr>Call</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktacall">Mfa<wbr>Policy<wbr>Okta<wbr>Call?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Okta<wbr>Otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaotp">Mfa<wbr>Policy<wbr>Okta<wbr>Otp?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Okta<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapassword">Mfa<wbr>Policy<wbr>Okta<wbr>Password?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Okta<wbr>Push</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapush">Mfa<wbr>Policy<wbr>Okta<wbr>Push?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Okta<wbr>Question</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaquestion">Mfa<wbr>Policy<wbr>Okta<wbr>Question?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Okta<wbr>Sms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktasms">Mfa<wbr>Policy<wbr>Okta<wbr>Sms?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Policy Priority, this attribute can be set to a valid priority. To avoid endless diff situation we error if an invalid
priority is provided. API defaults it to the last/lowest if not there.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Rsa<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyrsatoken">Mfa<wbr>Policy<wbr>Rsa<wbr>Token?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Policy Status: ACTIVE or INACTIVE.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Symantec<wbr>Vip</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicysymantecvip">Mfa<wbr>Policy<wbr>Symantec<wbr>Vip?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Yubikey<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyyubikeytoken">Mfa<wbr>Policy<wbr>Yubikey<wbr>Token?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Policy Description
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Duo</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyduo">*Mfa<wbr>Policy<wbr>Duo</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Fido<wbr>U2f</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidou2f">*Mfa<wbr>Policy<wbr>Fido<wbr>U2f</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Fido<wbr>Webauthn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidowebauthn">*Mfa<wbr>Policy<wbr>Fido<wbr>Webauthn</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Google<wbr>Otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicygoogleotp">*Mfa<wbr>Policy<wbr>Google<wbr>Otp</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Groups<wbr>Includeds</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of Group IDs to Include
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Policy Name
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Okta<wbr>Call</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktacall">*Mfa<wbr>Policy<wbr>Okta<wbr>Call</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Okta<wbr>Otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaotp">*Mfa<wbr>Policy<wbr>Okta<wbr>Otp</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Okta<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapassword">*Mfa<wbr>Policy<wbr>Okta<wbr>Password</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Okta<wbr>Push</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapush">*Mfa<wbr>Policy<wbr>Okta<wbr>Push</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Okta<wbr>Question</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaquestion">*Mfa<wbr>Policy<wbr>Okta<wbr>Question</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Okta<wbr>Sms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktasms">*Mfa<wbr>Policy<wbr>Okta<wbr>Sms</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Policy Priority, this attribute can be set to a valid priority. To avoid endless diff situation we error if an invalid
priority is provided. API defaults it to the last/lowest if not there.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Rsa<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyrsatoken">*Mfa<wbr>Policy<wbr>Rsa<wbr>Token</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Policy Status: ACTIVE or INACTIVE.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Symantec<wbr>Vip</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicysymantecvip">*Mfa<wbr>Policy<wbr>Symantec<wbr>Vip</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>Yubikey<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyyubikeytoken">*Mfa<wbr>Policy<wbr>Yubikey<wbr>Token</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Policy Description
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>duo</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyduo">Mfa<wbr>Policy<wbr>Duo?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>fido<wbr>U2f</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidou2f">Mfa<wbr>Policy<wbr>Fido<wbr>U2f?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>fido<wbr>Webauthn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidowebauthn">Mfa<wbr>Policy<wbr>Fido<wbr>Webauthn?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>google<wbr>Otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicygoogleotp">Mfa<wbr>Policy<wbr>Google<wbr>Otp?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>groups<wbr>Includeds</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}List of Group IDs to Include
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Policy Name
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>okta<wbr>Call</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktacall">Mfa<wbr>Policy<wbr>Okta<wbr>Call?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>okta<wbr>Otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaotp">Mfa<wbr>Policy<wbr>Okta<wbr>Otp?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>okta<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapassword">Mfa<wbr>Policy<wbr>Okta<wbr>Password?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>okta<wbr>Push</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapush">Mfa<wbr>Policy<wbr>Okta<wbr>Push?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>okta<wbr>Question</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaquestion">Mfa<wbr>Policy<wbr>Okta<wbr>Question?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>okta<wbr>Sms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktasms">Mfa<wbr>Policy<wbr>Okta<wbr>Sms?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Policy Priority, this attribute can be set to a valid priority. To avoid endless diff situation we error if an invalid
priority is provided. API defaults it to the last/lowest if not there.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>rsa<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyrsatoken">Mfa<wbr>Policy<wbr>Rsa<wbr>Token?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Policy Status: ACTIVE or INACTIVE.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>symantec<wbr>Vip</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicysymantecvip">Mfa<wbr>Policy<wbr>Symantec<wbr>Vip?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>yubikey<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyyubikeytoken">Mfa<wbr>Policy<wbr>Yubikey<wbr>Token?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-"
            title="">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Policy Description
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>duo</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyduo">Dict[Mfa<wbr>Policy<wbr>Duo]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>fido_<wbr>u2f</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidou2f">Dict[Mfa<wbr>Policy<wbr>Fido<wbr>U2f]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>fido_<wbr>webauthn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidowebauthn">Dict[Mfa<wbr>Policy<wbr>Fido<wbr>Webauthn]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>google_<wbr>otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicygoogleotp">Dict[Mfa<wbr>Policy<wbr>Google<wbr>Otp]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>groups_<wbr>includeds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}List of Group IDs to Include
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Policy Name
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>okta_<wbr>call</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktacall">Dict[Mfa<wbr>Policy<wbr>Okta<wbr>Call]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>okta_<wbr>otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaotp">Dict[Mfa<wbr>Policy<wbr>Okta<wbr>Otp]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>okta_<wbr>password</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapassword">Dict[Mfa<wbr>Policy<wbr>Okta<wbr>Password]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>okta_<wbr>push</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapush">Dict[Mfa<wbr>Policy<wbr>Okta<wbr>Push]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>okta_<wbr>question</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaquestion">Dict[Mfa<wbr>Policy<wbr>Okta<wbr>Question]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>okta_<wbr>sms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktasms">Dict[Mfa<wbr>Policy<wbr>Okta<wbr>Sms]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Policy Priority, this attribute can be set to a valid priority. To avoid endless diff situation we error if an invalid
priority is provided. API defaults it to the last/lowest if not there.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>rsa_<wbr>token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyrsatoken">Dict[Mfa<wbr>Policy<wbr>Rsa<wbr>Token]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Policy Status: ACTIVE or INACTIVE.
{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>symantec_<wbr>vip</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicysymantecvip">Dict[Mfa<wbr>Policy<wbr>Symantec<wbr>Vip]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-"
            title="">
        <span>yubikey_<wbr>token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyyubikeytoken">Dict[Mfa<wbr>Policy<wbr>Yubikey<wbr>Token]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}








## Look up an Existing MfaPolicy Resource

Get an existing MfaPolicy resource's state with the given name, ID, and optional extra properties used to qualify the lookup.

{{< chooser language "javascript,typescript,python,go,csharp  " / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span>: <span class="nx"><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/string">string</a></span><span class="p">, </span><span class="nx">id</span>: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">, </span><span class="nx">state</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/okta/deprecated/#MfaPolicyState">MfaPolicyState</a></span><span class="p">, </span><span class="nx">opts</span>?: <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/okta/deprecated/#MfaPolicy">MfaPolicy</a></span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">static </span><span class="nf">get</span><span class="p">(resource_name, id, opts=None, </span>description=None<span class="p">, </span>duo=None<span class="p">, </span>fido_u2f=None<span class="p">, </span>fido_webauthn=None<span class="p">, </span>google_otp=None<span class="p">, </span>groups_includeds=None<span class="p">, </span>name=None<span class="p">, </span>okta_call=None<span class="p">, </span>okta_otp=None<span class="p">, </span>okta_password=None<span class="p">, </span>okta_push=None<span class="p">, </span>okta_question=None<span class="p">, </span>okta_sms=None<span class="p">, </span>priority=None<span class="p">, </span>rsa_token=None<span class="p">, </span>status=None<span class="p">, </span>symantec_vip=None<span class="p">, </span>yubikey_token=None<span class="p">, __props__=None);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetMfaPolicy<span class="p">(</span><span class="nx">ctx</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#Context">Context</a></span><span class="p">, </span><span class="nx">name</span> <span class="nx"><a href="https://golang.org/pkg/builtin/#string">string</a></span><span class="p">, </span><span class="nx">id</span> <span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">, </span><span class="nx">state</span> *<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyState">MfaPolicyState</a></span><span class="p">, </span><span class="nx">opts</span> ...<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicy">MfaPolicy</a></span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Okta/Pulumi.Okta.Deprecated.MfaPolicy.html">MfaPolicy</a></span><span class="nf"> Get</span><span class="p">(</span><span class="nx"><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types">string</a></span> <span class="nx">name<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input.html">Input&lt;string&gt;</a></span> <span class="nx">id<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi.Okta/Pulumi.Okta.Deprecated.MfaPolicyState.html">MfaPolicyState</a></span>? <span class="nx">state<span class="p">, </span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>? <span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Policy Description
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Duo</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyduo">Mfa<wbr>Policy<wbr>Duo<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fido<wbr>U2f</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidou2f">Mfa<wbr>Policy<wbr>Fido<wbr>U2f<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fido<wbr>Webauthn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidowebauthn">Mfa<wbr>Policy<wbr>Fido<wbr>Webauthn<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Google<wbr>Otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicygoogleotp">Mfa<wbr>Policy<wbr>Google<wbr>Otp<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Groups<wbr>Includeds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List<string>?</span>
    </dt>
    <dd>{{% md %}}List of Group IDs to Include
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Policy Name
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Call</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktacall">Mfa<wbr>Policy<wbr>Okta<wbr>Call<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaotp">Mfa<wbr>Policy<wbr>Okta<wbr>Otp<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapassword">Mfa<wbr>Policy<wbr>Okta<wbr>Password<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Push</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapush">Mfa<wbr>Policy<wbr>Okta<wbr>Push<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Question</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaquestion">Mfa<wbr>Policy<wbr>Okta<wbr>Question<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Sms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktasms">Mfa<wbr>Policy<wbr>Okta<wbr>Sms<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">int?</span>
    </dt>
    <dd>{{% md %}}Policy Priority, this attribute can be set to a valid priority. To avoid endless diff situation we error if an invalid
priority is provided. API defaults it to the last/lowest if not there.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Rsa<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyrsatoken">Mfa<wbr>Policy<wbr>Rsa<wbr>Token<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Policy Status: ACTIVE or INACTIVE.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Symantec<wbr>Vip</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicysymantecvip">Mfa<wbr>Policy<wbr>Symantec<wbr>Vip<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Yubikey<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyyubikeytoken">Mfa<wbr>Policy<wbr>Yubikey<wbr>Token<wbr>Args?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Description</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Policy Description
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Duo</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyduo">*Mfa<wbr>Policy<wbr>Duo</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fido<wbr>U2f</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidou2f">*Mfa<wbr>Policy<wbr>Fido<wbr>U2f</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Fido<wbr>Webauthn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidowebauthn">*Mfa<wbr>Policy<wbr>Fido<wbr>Webauthn</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Google<wbr>Otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicygoogleotp">*Mfa<wbr>Policy<wbr>Google<wbr>Otp</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Groups<wbr>Includeds</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of Group IDs to Include
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Name</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Policy Name
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Call</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktacall">*Mfa<wbr>Policy<wbr>Okta<wbr>Call</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaotp">*Mfa<wbr>Policy<wbr>Okta<wbr>Otp</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapassword">*Mfa<wbr>Policy<wbr>Okta<wbr>Password</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Push</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapush">*Mfa<wbr>Policy<wbr>Okta<wbr>Push</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Question</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaquestion">*Mfa<wbr>Policy<wbr>Okta<wbr>Question</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Okta<wbr>Sms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktasms">*Mfa<wbr>Policy<wbr>Okta<wbr>Sms</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">*int</span>
    </dt>
    <dd>{{% md %}}Policy Priority, this attribute can be set to a valid priority. To avoid endless diff situation we error if an invalid
priority is provided. API defaults it to the last/lowest if not there.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Rsa<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyrsatoken">*Mfa<wbr>Policy<wbr>Rsa<wbr>Token</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Status</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}Policy Status: ACTIVE or INACTIVE.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Symantec<wbr>Vip</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicysymantecvip">*Mfa<wbr>Policy<wbr>Symantec<wbr>Vip</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Yubikey<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyyubikeytoken">*Mfa<wbr>Policy<wbr>Yubikey<wbr>Token</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Policy Description
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>duo</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyduo">Mfa<wbr>Policy<wbr>Duo?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fido<wbr>U2f</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidou2f">Mfa<wbr>Policy<wbr>Fido<wbr>U2f?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fido<wbr>Webauthn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidowebauthn">Mfa<wbr>Policy<wbr>Fido<wbr>Webauthn?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>google<wbr>Otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicygoogleotp">Mfa<wbr>Policy<wbr>Google<wbr>Otp?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>groups<wbr>Includeds</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]?</span>
    </dt>
    <dd>{{% md %}}List of Group IDs to Include
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Policy Name
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta<wbr>Call</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktacall">Mfa<wbr>Policy<wbr>Okta<wbr>Call?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta<wbr>Otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaotp">Mfa<wbr>Policy<wbr>Okta<wbr>Otp?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta<wbr>Password</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapassword">Mfa<wbr>Policy<wbr>Okta<wbr>Password?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta<wbr>Push</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapush">Mfa<wbr>Policy<wbr>Okta<wbr>Push?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta<wbr>Question</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaquestion">Mfa<wbr>Policy<wbr>Okta<wbr>Question?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta<wbr>Sms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktasms">Mfa<wbr>Policy<wbr>Okta<wbr>Sms?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">number?</span>
    </dt>
    <dd>{{% md %}}Policy Priority, this attribute can be set to a valid priority. To avoid endless diff situation we error if an invalid
priority is provided. API defaults it to the last/lowest if not there.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>rsa<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyrsatoken">Mfa<wbr>Policy<wbr>Rsa<wbr>Token?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}Policy Status: ACTIVE or INACTIVE.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>symantec<wbr>Vip</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicysymantecvip">Mfa<wbr>Policy<wbr>Symantec<wbr>Vip?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>yubikey<wbr>Token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyyubikeytoken">Mfa<wbr>Policy<wbr>Yubikey<wbr>Token?</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>description</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Policy Description
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>duo</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyduo">Dict[Mfa<wbr>Policy<wbr>Duo]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fido_<wbr>u2f</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidou2f">Dict[Mfa<wbr>Policy<wbr>Fido<wbr>U2f]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>fido_<wbr>webauthn</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyfidowebauthn">Dict[Mfa<wbr>Policy<wbr>Fido<wbr>Webauthn]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>google_<wbr>otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicygoogleotp">Dict[Mfa<wbr>Policy<wbr>Google<wbr>Otp]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>groups_<wbr>includeds</span>
        <span class="property-indicator"></span>
        <span class="property-type">List[str]</span>
    </dt>
    <dd>{{% md %}}List of Group IDs to Include
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Policy Name
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta_<wbr>call</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktacall">Dict[Mfa<wbr>Policy<wbr>Okta<wbr>Call]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta_<wbr>otp</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaotp">Dict[Mfa<wbr>Policy<wbr>Okta<wbr>Otp]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta_<wbr>password</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapassword">Dict[Mfa<wbr>Policy<wbr>Okta<wbr>Password]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta_<wbr>push</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktapush">Dict[Mfa<wbr>Policy<wbr>Okta<wbr>Push]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta_<wbr>question</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktaquestion">Dict[Mfa<wbr>Policy<wbr>Okta<wbr>Question]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>okta_<wbr>sms</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyoktasms">Dict[Mfa<wbr>Policy<wbr>Okta<wbr>Sms]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>priority</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}Policy Priority, this attribute can be set to a valid priority. To avoid endless diff situation we error if an invalid
priority is provided. API defaults it to the last/lowest if not there.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>rsa_<wbr>token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyrsatoken">Dict[Mfa<wbr>Policy<wbr>Rsa<wbr>Token]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>status</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Policy Status: ACTIVE or INACTIVE.
{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>symantec_<wbr>vip</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicysymantecvip">Dict[Mfa<wbr>Policy<wbr>Symantec<wbr>Vip]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>yubikey_<wbr>token</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#mfapolicyyubikeytoken">Dict[Mfa<wbr>Policy<wbr>Yubikey<wbr>Token]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}










## Supporting Types

<h4>Mfa<wbr>Policy<wbr>Duo</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/input/#MfaPolicyDuo">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/output/#MfaPolicyDuo">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyDuoArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyDuoOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Mfa<wbr>Policy<wbr>Fido<wbr>U2f</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/input/#MfaPolicyFidoU2f">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/output/#MfaPolicyFidoU2f">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyFidoU2fArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyFidoU2fOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Mfa<wbr>Policy<wbr>Fido<wbr>Webauthn</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/input/#MfaPolicyFidoWebauthn">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/output/#MfaPolicyFidoWebauthn">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyFidoWebauthnArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyFidoWebauthnOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Mfa<wbr>Policy<wbr>Google<wbr>Otp</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/input/#MfaPolicyGoogleOtp">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/output/#MfaPolicyGoogleOtp">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyGoogleOtpArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyGoogleOtpOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Mfa<wbr>Policy<wbr>Okta<wbr>Call</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/input/#MfaPolicyOktaCall">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/output/#MfaPolicyOktaCall">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyOktaCallArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyOktaCallOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Mfa<wbr>Policy<wbr>Okta<wbr>Otp</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/input/#MfaPolicyOktaOtp">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/output/#MfaPolicyOktaOtp">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyOktaOtpArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyOktaOtpOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Mfa<wbr>Policy<wbr>Okta<wbr>Password</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/input/#MfaPolicyOktaPassword">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/output/#MfaPolicyOktaPassword">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyOktaPasswordArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyOktaPasswordOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Mfa<wbr>Policy<wbr>Okta<wbr>Push</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/input/#MfaPolicyOktaPush">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/output/#MfaPolicyOktaPush">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyOktaPushArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyOktaPushOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Mfa<wbr>Policy<wbr>Okta<wbr>Question</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/input/#MfaPolicyOktaQuestion">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/output/#MfaPolicyOktaQuestion">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyOktaQuestionArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyOktaQuestionOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Mfa<wbr>Policy<wbr>Okta<wbr>Sms</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/input/#MfaPolicyOktaSms">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/output/#MfaPolicyOktaSms">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyOktaSmsArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyOktaSmsOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Mfa<wbr>Policy<wbr>Rsa<wbr>Token</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/input/#MfaPolicyRsaToken">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/output/#MfaPolicyRsaToken">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyRsaTokenArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyRsaTokenOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Mfa<wbr>Policy<wbr>Symantec<wbr>Vip</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/input/#MfaPolicySymantecVip">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/output/#MfaPolicySymantecVip">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicySymantecVipArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicySymantecVipOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}





<h4>Mfa<wbr>Policy<wbr>Yubikey<wbr>Token</h4>
{{% choosable language nodejs %}}
> See the <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/input/#MfaPolicyYubikeyToken">input</a> and <a href="/docs/reference/pkg/nodejs/pulumi/okta/types/output/#MfaPolicyYubikeyToken">output</a> API doc for this type.
{{% /choosable %}}

{{% choosable language go %}}
> See the <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyYubikeyTokenArgs">input</a> and <a href="https://pkg.go.dev/github.com/pulumi/pulumi-okta/sdk/go/okta/deprecated?tab=doc#MfaPolicyYubikeyTokenOutput">output</a> API doc for this type.
{{% /choosable %}}




{{% choosable language csharp %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language go %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>Consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>Enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">*string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language nodejs %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent<wbr>Type</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">string?</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}


{{% choosable language python %}}
<dl class="resources-properties">

    <dt class="property-optional"
            title="Optional">
        <span>consent_<wbr>type</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

    <dt class="property-optional"
            title="Optional">
        <span>enroll</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd>

</dl>
{{% /choosable %}}









<h3>Package Details</h3>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-okta">https://github.com/pulumi/pulumi-okta</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
    
</dl>

