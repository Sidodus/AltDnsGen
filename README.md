<h1 align= "center">
<img src="./public/AltDnsGeneratorLogo.PNG" alt="AltDns Generator Image">
<!-- <ins><em>AltDns Generator.js</em></ins> -->
</h1> 
<h6 align= "center" style="color: grey; margin-top: -10px"><small><a href="#">... #<em>AltDnsGenerator.js</em></a></small></h6><br />

<blockquote align="center" style="font-size: 1.5em">
    <em>AltDns Generator.js</em> Is An Application That Generates &amp; Intelligently Resolves Dynamic DNS Wildcards". </br></br>
</blockquote>
</hr>
<div align="center" style="font-size: 1.2em; font-weight: 900"><ins><em>AltDns Generator.js</em> Consists Of 3 Main, And 2 Optional Process</br></ins></div>
<ol>
  <li style="font-weight: 500"><em>Subdomain Wildcard Locator.js<sup>(01)</sup>: </em>
  <br/>
  <span style="color: grey; font-size: 0.9em; margin-left: 3em">Locates all possible wildcard points</span></li>
  <li style="font-weight: 500"><em>AltDns Generator.js<sup>(02)</sup>:</em>
  <br/>
  <span style="color: grey; font-size: 0.9em; margin-left: 3em">Generates potential DNS wildcards</span></li>
  <li style="font-weight: 500"><em>Set Wordlist Gen Parameters<sup>(03)</sup>:</em>
  <em>OPTIONAL</em>
  <br/>
  <span style="color: grey; font-size: 0.9em; margin-left: 3em">Set parameters for generating wordlist From domain names.</span></li>
  <li style="font-weight: 500"><em>DNS Resolver<sup>(04)</sup>:</em>
  <br/>
  <span style="color: grey; font-size: 0.9em; margin-left: 3em">Dynamically Resolves all generated wildcards</span></li>
   <li style="font-weight: 500"><em>Filter Params A From B<sup>(05)</sup>: </em>
   <em>OPTIONAL</em>
  <br/>
  <span style="color: grey; font-size: 0.9em; margin-left: 3em">Filter Params A From B And Return Unique Values In A or B & vice versa</span></li>
</ol>

<br />

<h2 align="center">How It Works</h2>
<h3>01). <ins><em>Subdomain Wildcard Locator.js</em></ins>:</h3>
<ul style="font-weight: 500">
  <li>Pass In Valid Subdomains</li>
  <li><em>Subdomain Wildcard Locator.js</em> Would  Process All The Subdomains And Return Only <em>UNIQUE</em> Subdomains (no duplicates) </li>
  <li><em>Subdomain Wildcard Locator.js</em> Would Then Process All The Unique Subdomains And Return All The <em>POTENTIAL</em> Wildcard Areas Within Those Subdomains <code>e.g *.exampledns.com</code></li> 
</ul>

<h3>02). <ins><em>AltDns Generator.js</em></ins>:</h3>
<ul style="font-weight: 500">
  <li><em>AltDns Generator.js </em> Takes In 2 Arguments</li>
    <ol>
      <li>DNS Wordlist</li>
      <li>Wildcard DNS Generated By <em>Subdomain Wildcard Locator.js</em> OR A Regular Domain <code>e.g *.exampledns.com OR dev.exampledns.com etc.</code> </li>
    </ol>
  <li><em>AltDns Generator.js </em> Treats Every Domain Independently Depending On Which Type Of Wildcard That Is Provided</li>
    <ol>
      <li>If The Supplied Subdomain Contains <code>*</code> As A Subdomain, Then <em>AltDns Generator.js </em> Would  Only Focus And Generate AltDns At The <code>*</code> Position Notwithstanding  If <code>Create All Possible AltDns Permutation</code> Is Checked</li>
      <li>If The Supplied Subdomain DOES NOT Contains <code>*</code> As A Subdomain, And <code>Create All Possible AltDns Permutation</code> Is NOT Checked, Then <em>AltDns Generator.js </em> Would  Only Focus On Generating AltDns At The Beginning Position Of The Supplied Domain
      <li>ELSE If The Supplied Subdomain DOES NOT Contains <code>*</code> As A Subdomain, And <code>Create All Possible AltDns Permutation</code> Is CHECKED, Then <em>AltDns Generator.js </em> Would Generate All Possible AltDns At At Every Position Of The Supplied Domain <br/> <code>e.g admin.dev.exampledns.com</code> & A Wordlist Of <code>git </code> Would Output <br/>
      <code>admin.dev.exampledns.com</code> <br/>
      <code>git.admin.dev.exampledns.com</code> <br/>
      <code>admin.git.dev.exampledns.com</code> <br/>
      <code>admin.dev.git.exampledns.com</code>
    </ol>
      <li>IF YOU ALREADY HAVE YOUR GENERATED DOMAINS & JUST WANT TO TEST IT'S VALIDITY WITHOUT NEEDING TO GENERATE NEW ALTDNS</li>
        <ul>
          <li>Input Your Domains Into The Domains Field</li>
          <li>Input <code>PASS</code> (in Caps) into the WordList Field.</li>
        </ul>
</ul>

<h3>03). <ins><em>Set Wordlist Generator Parameters</em></ins>:</h3>
  <code>OPTIONAL</code>
<ul style="font-weight: 500">
  <li>Setting Parameters For Generating Wordlist From Domain Names...
    <ol>
      <li>Set Min Word length To Return. <em>(default min length is 3)</em></li>
      <li>Set Max Word length To Return. <em>(default max length is 15)</em></li>
    </ol>
  </li>
</ul>

<h3>04). <ins><em>DNS Resolver</em></ins>:</h3>
<ul style="font-weight: 500">
  <li>Click On The <em>Resolve DNS</em> Button In The Menu Bar Of <em>AltDns Generator.js</em> An All Generated AltDns Would Be Sent To The Server For Processing</li>
  <li>Wait For <em>DNS Resolver</em> To Finish It's Job Then A Process Completion Message Would Appear On Your Screen & Result Would Be Populated As <em>Resolved DNS</em> OR Where It Fits Depending On The Outcome </li>
</ul>

<h3>05). <ins><em>Filter</em></ins>:</h3>
<code>OPTIONAL</code>
<ul style="font-weight: 500">
  <li>Filter Params A From B And Return The Unique Values In A</li>
  <li>Filter Params A From B And Return The Unique Values In B</li>
  <li>Filter Params A & B And Return The Unique Values In Both A & B</li>
</ul>

<h3><em><ins>Also</ins>:</em></h3>
<p>You Can Also Intelligently Resolve Domains In Bash Terminal (CMD) Using: <br/>

```sh
# Using .txt File Of Within 3000 Lines Of DNS (FAST)
# Note: A large file with lines over 3*** would return (xargs: argument line too long error)
cat inputDomains.txt | xargs -0 node resolveDns_bash.js | tee --append /locationTo/saveLiveDomains.txt

# Using .txt File Of Any Line Length Of DNS (SLOW)
# No Error With large file / Long Lines
cat inputDomains.txt | xargs -n 1 node resolveDns_bash.js | tee --append /locationTo/saveLiveDomains.txt

cat inputDomains.txt | xargs -n4 node resolveDns_bash.js | tee --append /locationTo/saveLiveDomains.txt
```

```js
// Using An Exported Array, From A .JS File Of Any Line Length OF DNS (FAST)
// No Error With large file / Long Lines
// NOTE: The "array" Argument is a constant & must be present in the code
node resolveDns_bash.js "/location/Of/dnsFunc.js" "array" | >> /locationTo/saveLiveDomains.txt

// dnsFunc.js File Example...
function dnsFunc() {
  let dns = [ "example.com", "www.example.com"];
  return dns;
}
module.exports = dnsFunc();
```

</p>

<p>"homepage": "https://sidodus.github.io/AltDnsGen/"</p>

> Use Online @ <a href="https://sidodus.github.io/AltDnsGen/" target="_blank" rel="noreferrer"> AltDnsGen</a>.
> <br/>
> Developed By <a href="https://www.linkedin.com/in/saheed-odulaja-75111337" target="_blank" rel="noreferrer"> Saheed Odulaja</a>.
