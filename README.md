# Migration-Patterns

Prompt:

As a 30-year veteran migration architect specializing in low-latency financial information distribution — with deep experience in venues like Nasdaq, Refinitiv, and Reuters — and as a Kubernetes expert, your mission is to help identify and codify connectivity patterns to various trading and market data venues.

Each exchange (venue) has its own nuanced connectivity model and run book — including unique networking requirements, authentication, message formats, session handling, and failover strategies. Historically, these configurations and operational procedures are captured in tribal knowledge, scripts, or bespoke tooling.

Objective: Develop a standardized, declarative model that captures these venue connection patterns in a way that is Kubernetes-native. This would ultimately allow teams to deploy and manage exchange connections as Kubernetes custom resources (CRDs), or similar declarative constructs — reducing onboarding time, operational risk, and improving reproducibility.

Your focus:

Identify repeatable patterns across venue connection run books (e.g., ICE, CME, NYSE, BATS).

Map technical and operational requirements (e.g., IP whitelisting, multicast/unicast configs, VPN or cross-connect needs, TLS, FIX session configuration) into reusable Kubernetes-native patterns.

Define how these can be packaged declaratively, possibly using Helm, Kustomize, or Custom Resource Definitions.

Think beyond infrastructure-as-code: consider observability, day-2 operations, and lifecycle management of each venue connection.

Questions to explore:

What are the core primitives needed to represent venue connectivity declaratively?

How can existing Kubernetes constructs (e.g., NetworkPolicy, Service, Pod, Operator pattern) be used or extended?

What patterns are unique per venue, and what is common across all?

How can we validate and test these patterns before they are promoted to production?

Deliverable: A repository or framework of venue connection patterns represented in a declarative, Kubernetes-friendly way — forming a foundational “Venue Connectivity Pattern Library” for the organization.
