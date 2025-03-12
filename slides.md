---
theme: default
background: 'https://cdn.sanity.io/images/4zrzovbb/website/3aabd8804251c0364cbde9d2e4be6dc8e8c2faec-2880x1620.png'
class: 'text-center'
highlighter: shiki
lineNumbers: false
info: |
  ## Model Context Protocol (MCP)
  A Developer's Guide to Seamless AI Integration
drawings:
  enabled: false
  persist: false
transition: slide-left
css: unocss
title: Model Context Protocol (MCP)
mdc: true
---

# Model Context Protocol

<!-- <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y--50">
  <h2 class="text-6xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-green-400 to-blue-500">
    Seamless AI Integration
  </h2>
</div> -->

<div class="abs-br m-6 flex gap-2">
  <a href="https://modelcontextprotocol.io" target="_blank" alt="MCP Website"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <i-carbon-logo-github />
  </a>
</div>

<!--
Presenter note: Welcome slide with gradient text effect
-->



---
layout: image-right
image: 'https://becomposable.com/hubfs/AI-Software-Marketscape-2025-01.jpg'
---

# The Challenge

<v-clicks>

<div class="flex items-center mb-6">
  <div class="mr-4 p-3 rounded-full bg-red-500 bg-opacity-20">
    <i-carbon-warning-alt class="text-2xl text-red-500"/>
  </div>
  <div class="flex-1">
    <div class="font-bold mb-1">Fragmented AI Landscape</div>
    <div class="text-sm opacity-80">Multiple AI providers, each with unique APIs, authentication methods, and data formats, making integration complex and time-consuming.</div>
  </div>
</div>

<div class="flex items-center mb-6">
  <div class="mr-4 p-3 rounded-full bg-orange-500 bg-opacity-20">
    <i-carbon-development class="text-2xl text-orange-500"/>
  </div>
  <div class="flex-1">
    <div class="font-bold mb-1">Complex Integration</div>
    <div class="text-sm opacity-80">Diverse tooling, context management, and unique response handling create development overhead for custom implementations.</div>
  </div>
</div>

<div class="flex items-center mb-6">
  <div class="mr-4 p-3 rounded-full bg-yellow-500 bg-opacity-20">
    <i-carbon-security class="text-2xl text-yellow-500"/>
  </div>
  <div class="flex-1">
    <div class="font-bold mb-1">Security Concerns</div>
    <div class="text-sm opacity-80">Data privacy, access control, and secure communication channels pose critical challenges when integrating AI capabilities.</div>
  </div>
</div>

</v-clicks>

<div class="mt-8 grid grid-cols-3 gap-4">
  <div v-click class="text-center p-4 rounded-lg bg-red-500 bg-opacity-10">
    <i-carbon-cloud-services class="text-3xl text-red-400 mb-2"/>
    <div class="text-sm opacity-80">Growing Number of AI Services</div>
  </div>
  <div v-click class="text-center p-4 rounded-lg bg-orange-500 bg-opacity-10">
    <i-carbon-time class="text-3xl text-orange-400 mb-2"/>
    <div class="text-sm opacity-80">Increasing application complexity</div>
  </div>
  <div v-click class="text-center p-4 rounded-lg bg-yellow-500 bg-opacity-10">
    <i-carbon-shield class="text-3xl text-yellow-400 mb-2"/>
    <div class="text-sm opacity-80">Development time and costs rise</div>
  </div>
</div>

---
layout: fact
---

<div class="text-center">
  <h1 class="text-8xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-green-400 to-blue-500">
    Enter MCP
  </h1>
  <p class="mt-4 text-2xl opacity-80">Model Context Protocol</p>
  <p class="mt-2 text-xl opacity-60">The missing standard for AI integration</p>
</div>

<!-- 
This is where Model Context Protocol comes in - a standardized approach to solve these challenges.
-->

---
layout: default
transition: slide-up
---

# What is MCP?

<div 
  class="text-center transition-all duration-500 absolute left-1/2 transform -translate-x-1/2"
  :class="{ 'top-1/2 -translate-y-1/2': $slidev.nav.clicks === 0, 'top-24': $slidev.nav.clicks > 0 }"
>
  <p class="text-xl max-w-4xl w-[800px] font-bold text-gray-800">
    MCP is an open protocol that enables seamless integration between AI apps and agents and tools and data sources
  </p>
</div>

<div 
  v-if="$slidev.nav.clicks > 0" 
  class="relative mt-28 p-6 rounded-lg overflow-hidden animate-fade-in"
>
  <div class="absolute inset-0 bg-gradient-to-br from-blue-500/20 to-purple-500/20 rounded-lg"></div>
  <div class="relative z-10">
    <div class="flex items-center justify-center mb-4">
      <div class="text-center">
        <i-carbon-api-1 class="text-5xl text-blue-400 inline-block"/>
        <i-carbon-arrow-right class="text-3xl text-gray-400 mx-2 inline-block"/>
        <i-carbon-application-web class="text-5xl text-green-400 inline-block"/>
        <p class="mt-2 font-bold text-lg">APIs in Web Development</p>
        <p class="text-sm opacity-80">Connect applications to data and services</p>
      </div>
      <div class="mx-8 text-3xl opacity-30">=</div>
      <div class="text-center">
        <i-carbon-machine-learning-model class="text-5xl text-purple-400 inline-block"/>
        <i-carbon-arrow-right class="text-3xl text-gray-400 mx-2 inline-block"/>
        <i-carbon-tool-kit class="text-5xl text-pink-400 inline-block"/>
        <p class="mt-2 font-bold text-lg">MCP in AI Ecosystem</p>
        <p class="text-sm opacity-80">Connects AI applications to tools and data</p>
      </div>
    </div>
    <!-- 
    Just as APIs provide a standardized way for web applications to interact with data services, MCP offers a uniform interface for LLMs and generative AI to access tools, context, and data sources - eliminating the need for custom integration with each AI provider.
    -->
  </div>
</div>

<div v-click class="mt-8 grid grid-cols-3 gap-4" :class="{ 'opacity-0': $slidev.nav.clicks < 1, 'opacity-100 transition-opacity duration-500 delay-300': $slidev.nav.clicks >= 1 }">
  <div class="relative group p-4 rounded-lg overflow-hidden transition-all duration-500 hover:scale-105">
    <div class="absolute inset-0 bg-gradient-to-br from-blue-500/30 to-blue-700/30 group-hover:opacity-100 transition-opacity"></div>
    <div class="relative z-10">
      <i-carbon-api class="text-4xl mb-3 text-blue-400"/>
      <div class="font-bold text-xl mb-2">Open Standard</div>
      <div class="text-sm opacity-80 leading-relaxed">An open protocol designed for community adoption and extension</div>
    </div>
  </div>
  
  <div class="relative group p-4 rounded-lg overflow-hidden transition-all duration-500 hover:scale-105">
    <div class="absolute inset-0 bg-gradient-to-br from-green-500/30 to-green-700/30 group-hover:opacity-100 transition-opacity"></div>
    <div class="relative z-10">
      <i-carbon-tool-kit class="text-4xl mb-3 text-green-400"/>
      <div class="font-bold text-xl mb-2">Tool Integration</div>
      <div class="text-sm opacity-80 leading-relaxed">Securely connect AI with your application's tools and capabilities</div>
    </div>
  </div>
  
  <div class="relative group p-4 rounded-lg overflow-hidden transition-all duration-500 hover:scale-105">
    <div class="absolute inset-0 bg-gradient-to-br from-purple-500/30 to-purple-700/30 group-hover:opacity-100 transition-opacity"></div>
    <div class="relative z-10">
      <i-carbon-data-enrichment class="text-4xl mb-3 text-purple-400"/>
      <div class="font-bold text-xl mb-2">Data Access</div>
      <div class="text-sm opacity-80 leading-relaxed">Controlled access to application resources and contextual data</div>
    </div>
  </div>
</div>

<style>
.animate-fade-in {
  animation: fadeIn 0.8s ease-out forwards;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>


---
layout: image-right
image: 'servers_screenshot.png'
---

# Growing MCP Support

<div class="flex flex-col gap-4 pr-0">
  <div class="relative group">
    <div class="absolute -inset-0.5 bg-gradient-to-r from-blue-500 to-indigo-500 rounded-lg blur opacity-30 group-hover:opacity-100 transition duration-1000"></div>
    <div class="relative p-5 bg-gray-900 rounded-lg border border-blue-500/30">
      <div class="flex items-center mb-4">
        <i-carbon-repository class="text-4xl text-blue-400 mr-3"/>
        <div>
          <div class="font-bold text-lg text-blue-300">Official MCP Servers Repository</div>
          <div class="text-sm text-gray-300">11.4k+ stars · 1.2k+ forks · 200+ contributors</div>
        </div>
      </div>
      <p class="text-gray-200 text-sm mb-4">Collection of reference MCP servers.</p>
      <div class="grid grid-cols-3 gap-2">
        <div class="bg-gray-800 rounded px-3 py-2 text-gray-300 text-xs">
          <i-carbon-document class="mr-1 text-blue-400"/> GitHub
        </div>
        <div class="bg-gray-800 rounded px-3 py-2 text-gray-300 text-xs">
          <i-carbon-delivery class="mr-1 text-green-400"/> Jira
        </div>
        <div class="bg-gray-800 rounded px-3 py-2 text-gray-300 text-xs">
          <i-carbon-shopping-catalog class="mr-1 text-yellow-400"/> PostgreSQL
        </div>
        <div class="bg-gray-800 rounded px-3 py-2 text-gray-300 text-xs">
          <i-carbon-cloud class="mr-1 text-purple-400"/> Weather
        </div>
        <div class="bg-gray-800 rounded px-3 py-2 text-gray-300 text-xs">
          <i-carbon-search class="mr-1 text-red-400"/> Google
        </div>
        <div class="bg-gray-800 rounded px-3 py-2 text-gray-300 text-xs">
          <i-carbon-folder class="mr-1 text-orange-400"/> FileSystem
        </div>
      </div>
    </div>
  </div>

  <div class="relative group">
    <div class="absolute -inset-0.5 bg-gradient-to-r from-green-500 to-teal-500 rounded-lg blur opacity-30 group-hover:opacity-100 transition duration-1000"></div>
    <div class="relative p-5 bg-gray-900 rounded-lg border border-green-500/30">
      <div class="flex items-center mb-4">
        <i-carbon-connect class="text-4xl text-green-400 mr-3"/>
        <div>
          <div class="font-bold text-lg text-green-300">Community-Created Servers</div>
          <div class="text-sm text-gray-300">500+ servers in the awesome-mcp-servers list</div>
        </div>
      </div>
      <div class="grid grid-cols-2 gap-3">
        <div class="flex items-start p-2 bg-gray-800 rounded">
          <i-carbon-diagram class="text-teal-400 mt-1 mr-2 flex-shrink-0"/>
          <div>
            <div class="text-sm text-gray-300">JetBrains</div>
          </div>
        </div>
        <div class="flex items-start p-2 bg-gray-800 rounded">
          <i-carbon-network-3 class="text-blue-400 mt-1 mr-2 flex-shrink-0"/>
          <div>
            <div class="text-sm text-gray-300">Bluesky</div>
          </div>
        </div>
        <div class="flex items-start p-2 bg-gray-800 rounded">
          <i-carbon-currency-bitcoin class="text-yellow-400 mt-1 mr-2 flex-shrink-0"/>
          <div>
            <div class="text-sm text-gray-300">Binance</div>
          </div>
        </div>
        <div class="flex items-start p-2 bg-gray-800 rounded">
          <i-carbon-document-pdf class="text-red-400 mt-1 mr-2 flex-shrink-0"/>
          <div>
            <div class="text-sm text-gray-300">Box</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- 
Right side placeholder:
In the layout: image-right format, you need to replace the image: '#' with the actual screenshot URL.
Example: image: 'path/to/mcp-servers-screenshot.png'
-->

<!--
This slide showcases the rapidly growing ecosystem of MCP servers. The official MCP servers repository has gained incredible traction with over 11,000 stars and 1,200+ forks on GitHub, demonstrating strong community interest. The community has extended beyond the official implementations, with hundreds of third-party servers being developed for diverse use cases from social media integration to financial services.
-->

---
layout: default
---

# Core Architecture

<div class="mt-15 h-[200px] flex items-center justify-center">

```mermaid {theme: 'neutral', scale: 0.5}
graph TB
    subgraph Host["Host Application (e.g., IDE, Claude Desktop)"]
        H[Host Application]
        subgraph Client["MCP Client"]
            CL[Client Layer]
            CPL[Protocol Layer]
            CTL[Transport Layer]
            CL --> CPL --> CTL
        end
        H --- CL
    end
    
    subgraph Server["MCP Server"]
        SL[Server Layer]
        SPL[Protocol Layer]
        STL[Transport Layer]
        
        SL --> SPL --> STL
        
        subgraph Capabilities["Server Capabilities"]
            CAP1[Resources]
            CAP2[Tools]
            CAP3[Context]
            CAP4[Prompts]
            
            SL --> CAP1
            SL --> CAP2
            SL --> CAP3
            SL --> CAP4
        end
    end
    
    %% Communication Channels
    CTL <--> |JSON-RPC 2.0| STL
    
    %% Transport Options
    subgraph Transport["Transport Mechanisms"]
        T1[Stdio Transport]
        T2[HTTP with SSE]
        
        T1 --> CTL
        T2 --> CTL
    end
    
    %% Styling
    classDef default fill:#2A2A2A,stroke:#666,stroke-width:6px,color:#fff
    classDef primary fill:#3b82f6,stroke:#60a5fa,stroke-width:6px,color:#fff
    classDef secondary fill:#10b981,stroke:#34d399,stroke-width:6px,color:#fff
    classDef tertiary fill:#8b5cf6,stroke:#a78bfa,stroke-width:6px,color:#fff
    classDef container fill:transparent,stroke:#666,stroke-width:2px
    
    class H,CL,SL primary
    class CPL,SPL,CTL,STL secondary
    class CAP1,CAP2,CAP3,CAP4 tertiary
    class T1,T2 secondary
    class Host,Client,Server,Capabilities,Transport container

    %% Add thicker lines for connections
    linkStyle default stroke-width:3px
```

</div>

<div class="mt-20 grid grid-cols-3 gap-4">
  <div v-click class="relative group p-4 rounded-lg overflow-hidden transition-all duration-500 hover:scale-105">
    <div class="absolute inset-0 bg-gradient-to-br from-blue-500/30 to-blue-700/30 group-hover:opacity-100 transition-opacity"></div>
    <div class="relative z-10">
      <i-carbon-application-web class="text-3xl mb-2 text-blue-400"/>
      <div class="font-bold">Host Layer</div>
      <div class="text-sm opacity-80">LLM Applications that want to access data through MCP</div>
    </div>
  </div>
  <div v-click class="relative group p-4 rounded-lg overflow-hidden transition-all duration-500 hover:scale-105">
    <div class="absolute inset-0 bg-gradient-to-br from-green-500/30 to-green-700/30 group-hover:opacity-100 transition-opacity"></div>
    <div class="relative z-10">
      <i-carbon-connect class="text-3xl mb-2 text-green-400"/>
      <div class="font-bold">Client Layer</div>
      <div class="text-sm opacity-80">Maintains and manages 1:1 connections to MCP Servers</div>
    </div>
  </div>
  <div v-click class="relative group p-4 rounded-lg overflow-hidden transition-all duration-500 hover:scale-105">
    <div class="absolute inset-0 bg-gradient-to-br from-purple-500/30 to-purple-700/30 group-hover:opacity-100 transition-opacity"></div>
    <div class="relative z-10">
      <i-carbon-machine-learning-model class="text-3xl mb-2 text-purple-400"/>
      <div class="font-bold">Server Layer</div>
      <div class="text-sm opacity-80">Provides data, tools and prompts to Clients</div>
    </div>
  </div>
</div>

---
layout: default
---

# Key Components

<div class="mt-6 grid grid-cols-2 gap-8">
  <div v-click class="relative group">
    <div class="absolute -inset-0.5 bg-gradient-to-r from-blue-500 to-green-500 rounded-lg blur opacity-30 group-hover:opacity-100 transition duration-1000"></div>
    <div class="relative p-4 bg-gray-900 rounded-lg border border-blue-500/30">
      <h3 class="text-xl font-bold mb-4 text-blue-400">Protocol Layer</h3>
      <div class="space-y-2 text-sm">
        <div class="flex items-center text-gray-200">
          <i-carbon-data-share class="mr-2 text-blue-400"/> Message Framing & Routing
        </div>
        <div class="flex items-center text-gray-200">
          <i-carbon-connect class="mr-2 text-blue-400"/> Request/Response Management
        </div>
        <div class="flex items-center text-gray-200">
          <i-carbon-flow class="mr-2 text-blue-400"/> Communication Patterns
        </div>
        <div class="flex items-center text-gray-200">
          <i-carbon-certificate class="mr-2 text-blue-400"/> Versioned Protocol Schemas
        </div>
      </div>
    </div>
  </div>

  <div v-click class="relative group">
    <div class="absolute -inset-0.5 bg-gradient-to-r from-purple-500 to-pink-500 rounded-lg blur opacity-30 group-hover:opacity-100 transition duration-1000"></div>
    <div class="relative p-4 bg-gray-900 rounded-lg border border-purple-500/30">
      <h3 class="text-xl font-bold mb-4 text-purple-400">Transport Layer</h3>
      <div class="space-y-2 text-sm">
        <div class="flex items-center text-gray-200">
          <i-carbon-code class="mr-2 text-purple-400"/> JSON-RPC 2.0 Wire Format
        </div>
        <div class="flex items-center text-gray-200">
          <i-carbon-data-transformer class="mr-2 text-purple-400"/> Protocol Message Transmission
        </div>
        <div class="flex items-center text-gray-200">
          <i-carbon-terminal class="mr-2 text-purple-400"/> Multiple Transport Methods
        </div>
        <div class="flex items-center text-gray-200">
          <i-carbon-plug class="mr-2 text-purple-400"/> Extensible Channel System
        </div>
      </div>
    </div>
  </div>
</div>

<div v-click class="mt-8">
  <div class="relative group">
    <div class="absolute -inset-0.5 bg-gradient-to-r from-yellow-500 to-red-500 rounded-lg blur opacity-30 group-hover:opacity-100 transition duration-1000"></div>
    <div class="relative p-4 bg-gray-900 rounded-lg border border-yellow-500/30">
      <div class="grid grid-cols-3 gap-8 text-sm">
        <div class="text-center">
          <div class="mb-1 text-gray-400 text-[10px] uppercase tracking-wide">Model-controlled</div>
          <i-carbon-tool-kit class="text-3xl mb-2 mx-auto text-yellow-400"/> 
          <div class="text-gray-200 font-semibold">Tools</div>
          <div class="text-xs text-gray-400">Functions invoked by the model</div>
          <div class="mt-3 space-y-1">
            <div class="bg-gray-800 rounded px-3 py-1 text-gray-300">Retrieve / search</div>
            <div class="bg-gray-800 rounded px-3 py-1 text-gray-300">Send a message</div>
            <div class="bg-gray-800 rounded px-3 py-1 text-gray-300">Update DB records</div>
          </div>
        </div>
        <div class="text-center">
          <div class="mb-1 text-gray-400 text-[10px] uppercase tracking-wide">Application-controlled</div>
          <i-carbon-document class="text-3xl mb-2 mx-auto text-yellow-400"/> 
          <div class="text-gray-200 font-semibold">Resources</div>
          <div class="text-xs text-gray-400">Data exposed to the application</div>
          <div class="mt-3 space-y-1">
            <div class="bg-gray-800 rounded px-3 py-1 text-gray-300">Files</div>
            <div class="bg-gray-800 rounded px-3 py-1 text-gray-300">Database Records</div>
            <div class="bg-gray-800 rounded px-3 py-1 text-gray-300">API Responses</div>
          </div>
        </div>
        <div class="text-center">
          <div class="mb-1 text-gray-400 text-[10px] uppercase tracking-wide">User-controlled</div>
          <i-carbon-text-creation class="text-3xl mb-2 mx-auto text-yellow-400"/> 
          <div class="text-gray-200 font-semibold">Prompts</div>
          <div class="text-xs text-gray-400">Pre-defined templates for AI interactions</div>
          <div class="mt-3 space-y-1">
            <div class="bg-gray-800 rounded px-3 py-1 text-gray-300">Document Q&A</div>
            <div class="bg-gray-800 rounded px-3 py-1 text-gray-300">Transcript Summary</div>
            <div class="bg-gray-800 rounded px-3 py-1 text-gray-300">Workflow Automation</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<!--
Speaker notes:

The Protocol Layer and Transport Layer have distinct responsibilities in MCP:

- Protocol Layer: Handles the logical aspects of communication
  - Message framing: Structures messages in a consistent format
  - Request/response linking: Ensures requests are matched with corresponding responses
  - Communication patterns: Manages high-level communication flows between clients and servers
  - Schema validation: Validates messages against versioned schemas

- Transport Layer: Handles the physical communication mechanisms
  - Implements specific transport methods (Stdio, HTTP/SSE, WebSockets)
  - Uses JSON-RPC 2.0 as the wire format for message exchange
  - Converts MCP protocol messages into JSON-RPC format for transmission
  - Converts received JSON-RPC messages back into MCP protocol messages

Think of the Protocol Layer as defining "what" messages mean, while the Transport Layer determines "how" they are delivered. The Protocol Layer is transport-agnostic, allowing MCP to work across different communication channels.
-->

---
layout: default
transition: slide-up
---

# Sampling in MCP

<div 
  class="text-center transition-all duration-500 absolute left-1/2 transform -translate-x-1/2"
  :class="{ 'top-1/2 -translate-y-1/2': $slidev.nav.clicks === 0, 'top-23': $slidev.nav.clicks > 0 }"
>
  <p class="text-xl max-w-4xl w-[800px] font-bold text-gray-800">
    Enabling sophisticated agentic behaviors while maintaining security and privacy
  </p>
</div>

<div class="grid grid-cols-2 gap-8 mt-20" :class="{ 'opacity-0': $slidev.nav.clicks < 1, 'opacity-100 transition-opacity duration-500': $slidev.nav.clicks >= 1 }">
  <div class="relative group">
    <div class="absolute -inset-0.5 bg-gradient-to-r from-orange-500 to-amber-500 rounded-lg blur opacity-30 group-hover:opacity-100 transition duration-1000"></div>
    <div class="relative p-4 bg-gray-900 rounded-lg border border-orange-500/30">
      <h3 class="text-xl font-bold mb-4 text-orange-400">What is MCP Sampling?</h3>
      <div class="space-y-3 text-sm">
        <div class="flex items-start">
          <i-carbon-ibm-watson-knowledge-studio class="mr-2 text-orange-400 mt-1 flex-shrink-0"/> 
          <span class="text-gray-200">Allows Servers to request LLM completions through Client</span>
        </div>
        <div class="flex items-start">
          <i-carbon-user-role class="mr-2 text-orange-400 mt-1 flex-shrink-0"/> 
          <span class="text-gray-200">Human-in-the-loop design</span>
        </div>
        <div class="flex items-start">
          <i-carbon-data-reference class="mr-2 text-orange-400 mt-1 flex-shrink-0"/> 
          <span class="text-gray-200">Contextual awareness with controlled data sharing</span>
        </div>
        <div class="flex items-start">
          <i-carbon-data-reference class="mr-2 text-orange-400 mt-1 flex-shrink-0"/> 
          <span class="text-gray-200">Conversation history, Model preferences and prompts</span>
        </div>
      </div>
    </div>
  </div>

  <div class="relative group">
    <div class="absolute -inset-0.5 bg-gradient-to-r from-teal-500 to-green-500 rounded-lg blur opacity-30 group-hover:opacity-100 transition duration-1000"></div>
    <div class="relative p-4 bg-gray-900 rounded-lg border border-teal-500/30">
      <h3 class="text-xl font-bold mb-4 text-teal-400">Agentic Capabilities</h3>
      <div class="space-y-3 text-sm">
        <div class="flex items-start">
          <i-carbon-document-sentiment class="mr-2 text-teal-400 mt-1 flex-shrink-0"/> 
          <span class="text-gray-200">Reading and analyzing resources with context awareness</span>
        </div>
        <div class="flex items-start">
          <i-carbon-decision class="mr-2 text-teal-400 mt-1 flex-shrink-0"/> 
          <span class="text-gray-200">Making intelligent decisions based on contextual data</span>
        </div>
        <div class="flex items-start">
          <i-carbon-data-structured class="mr-2 text-teal-400 mt-1 flex-shrink-0"/> 
          <span class="text-gray-200">Generating structured data and formatted responses</span>
        </div>
        <div class="flex items-start">
          <i-carbon-workflow-automation class="mr-2 text-teal-400 mt-1 flex-shrink-0"/> 
          <span class="text-gray-200">Handling multi-step tasks with interactive assistance</span>
        </div>
      </div>
    </div>
  </div>
</div>

<div v-click class="mt-8" :class="{ 'opacity-0': $slidev.nav.clicks < 1, 'opacity-100 transition-opacity duration-500 delay-300': $slidev.nav.clicks >= 1 }">
  <div class="relative group">
    <div class="absolute -inset-0.5 bg-gradient-to-r from-blue-500 to-indigo-500 rounded-lg blur opacity-30 group-hover:opacity-100 transition duration-1000"></div>
    <div class="relative p-5 bg-gray-900 rounded-lg border border-blue-500/30">
      <h3 class="text-center text-lg font-bold mb-3 text-blue-400">Sampling Flow</h3>
      <div class="mx-auto w-full max-w-4xl">
        <div class="flex justify-between items-center text-center">
          <div class="bg-gray-800 rounded-lg p-2 w-[18%]">
            <i-carbon-server class="text-3xl mb-1 mx-auto text-purple-400"/>
            <div class="text-xs text-gray-200">Server Requests Completion</div>
          </div>
          <i-carbon-arrow-right class="text-gray-400"/>
          <div class="bg-gray-800 rounded-lg p-2 w-[18%]">
            <i-carbon-user-admin class="text-3xl mb-1 mx-auto text-blue-400"/>
            <div class="text-xs text-gray-200">Client Reviews Request</div>
          </div>
          <i-carbon-arrow-right class="text-gray-400"/>
          <div class="bg-gray-800 rounded-lg p-2 w-[18%]">
            <i-carbon-machine-learning-model class="text-3xl mb-1 mx-auto text-green-400"/>
            <div class="text-xs text-gray-200">LLM Generates Response</div>
          </div>
          <i-carbon-arrow-right class="text-gray-400"/>
          <div class="bg-gray-800 rounded-lg p-2 w-[18%]">
            <i-carbon-user-role class="text-3xl mb-1 mx-auto text-yellow-400"/>
            <div class="text-xs text-gray-200">Client Reviews Output</div>
          </div>
          <i-carbon-arrow-right class="text-gray-400"/>
          <div class="bg-gray-800 rounded-lg p-2 w-[18%]">
            <i-carbon-application-web class="text-3xl mb-1 mx-auto text-red-400"/>
            <div class="text-xs text-gray-200">Result Returns to Server</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<!--
This slide explains MCP sampling as a powerful feature enabling servers to request LLM completions through clients, facilitating sophisticated agentic workflows while maintaining human oversight. The human-in-the-loop design ensures users maintain control over what the LLM sees and generates, balancing powerful automation with security and privacy.
-->

---
layout: default
---

# MCP in Action: Demo

<div class="mt-2 mb-4 text-center">
  <p class="text-lg max-w-3xl mx-auto text-gray-800">
    See how MCP sampling enables powerful agentic workflows in real-world applications
  </p>
</div>

<div class="flex justify-center items-center mt-4">
  <div class="relative w-[700px] h-[400px] bg-gray-900 rounded-lg overflow-hidden border-2 border-gray-700 flex items-center justify-center">
    <!-- Video will be embedded here -->
    <div class="text-center">
      <i-carbon-play-filled class="text-5xl text-gray-600 mb-3"/>
      <p class="text-lg text-gray-500">Video placeholder</p>
      <p class="text-sm text-gray-600 mt-1">Video will be added here</p>
    </div>
    
    <!-- Uncomment and update the src when you have the video -->
    <!-- 
    <video 
      controls
      class="w-full h-full object-cover"
      poster="path/to/optional-poster-image.jpg">
      <source src="path/to/your-video.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    -->
  </div>
</div>

<!--
This slide demonstrates MCP in action with a real-world example. The video shows how sampling enables sophisticated agentic behaviors while maintaining user control.
-->

---
layout: default
---

# The Future of MCP

<div class="mt-8 mb-6 text-center">
  <p class="text-xl max-w-3xl mx-auto text-gray-800">
    <strong>THE POWER OF MCP IS ONLY GOING TO GROW</strong>
    </p>
    <p class="text-lg max-w-3xl mx-auto text-gray-600">
    The current development road map looks like:
  </p>
</div>

<div class="grid grid-cols-2 gap-8">
  <div v-click class="relative group">
    <div class="absolute -inset-0.5 bg-gradient-to-r from-blue-500 to-purple-500 rounded-lg blur opacity-30 group-hover:opacity-100 transition duration-1000"></div>
    <div class="relative p-4 bg-gray-900 rounded-lg border border-blue-500/30">
      <h3 class="text-xl font-bold mb-4 text-blue-400">Remote MCP Support</h3>
      <div class="space-y-2 text-sm">
        <div class="flex items-start">
          <i-carbon-security class="mr-2 text-blue-400 mt-1 flex-shrink-0"/> 
          <span class="text-gray-200">Authentication & Authorization with OAuth 2.0</span>
        </div>
        <div class="flex items-start">
          <i-carbon-network-4 class="mr-2 text-blue-400 mt-1 flex-shrink-0"/> 
          <span class="text-gray-200">Service Discovery for remote connections</span>
        </div>
        <div class="flex items-start">
          <i-carbon-cloud class="mr-2 text-blue-400 mt-1 flex-shrink-0"/> 
          <span class="text-gray-200">Stateless operations for serverless environments</span>
        </div>
      </div>
    </div>
  </div>

  <div v-click class="relative group">
    <div class="absolute -inset-0.5 bg-gradient-to-r from-green-500 to-teal-500 rounded-lg blur opacity-30 group-hover:opacity-100 transition duration-1000"></div>
    <div class="relative p-4 bg-gray-900 rounded-lg border border-green-500/30">
      <h3 class="text-xl font-bold mb-4 text-green-400">Advanced Agent Support</h3>
      <div class="space-y-2 text-sm">
        <div class="flex items-start">
          <i-carbon-tree-view-alt class="mr-2 text-green-400 mt-1 flex-shrink-0"/> 
          <span class="text-gray-200">Hierarchical agent systems with namespacing</span>
        </div>
        <div class="flex items-start">
          <i-carbon-flow class="mr-2 text-green-400 mt-1 flex-shrink-0"/> 
          <span class="text-gray-200">Interactive workflows with permission management</span>
        </div>
        <div class="flex items-start">
          <i-carbon-data-player class="mr-2 text-green-400 mt-1 flex-shrink-0"/> 
          <span class="text-gray-200">Streaming results for real-time agent operations</span>
        </div>
      </div>
    </div>
  </div>
</div>

<div v-click class="mt-8 grid grid-cols-3 gap-4">
  <div class="relative group p-4 rounded-lg overflow-hidden transition-all duration-500 hover:scale-105">
    <div class="absolute inset-0 bg-gradient-to-br from-yellow-500/30 to-amber-700/30 group-hover:opacity-100 transition-opacity"></div>
    <div class="relative z-10">
      <i-carbon-package class="text-3xl mb-2 text-yellow-400"/>
      <div class="font-bold">Distribution & Discovery</div>
      <div class="text-sm opacity-80">Standardized packaging and server registry</div>
    </div>
  </div>
  
  <div class="relative group p-4 rounded-lg overflow-hidden transition-all duration-500 hover:scale-105">
    <div class="absolute inset-0 bg-gradient-to-br from-purple-500/30 to-indigo-700/30 group-hover:opacity-100 transition-opacity"></div>
    <div class="relative z-10">
      <i-carbon-video class="text-3xl mb-2 text-purple-400"/>
      <div class="font-bold">Additional Modalities</div>
      <div class="text-sm opacity-80">Expanding beyond text to audio, video, and more</div>
    </div>
  </div>
  
  <div class="relative group p-4 rounded-lg overflow-hidden transition-all duration-500 hover:scale-105">
    <div class="absolute inset-0 bg-gradient-to-br from-red-500/30 to-pink-700/30 group-hover:opacity-100 transition-opacity"></div>
    <div class="relative z-10">
      <i-carbon-collaborate class="text-3xl mb-2 text-red-400"/>
      <div class="font-bold">Community-Led Standards</div>
      <div class="text-sm opacity-80">Open governance and standardization initiatives</div>
    </div>
  </div>
</div>

<!--
This slide outlines the future roadmap for MCP, highlighting key initiatives planned for 2025 and beyond. The focus areas include enabling remote connections, enhancing agent capabilities, improving distribution mechanisms, supporting new modalities beyond text, and fostering community-led standards development. These initiatives aim to make MCP more accessible, powerful, and widely adopted across the AI ecosystem.
-->