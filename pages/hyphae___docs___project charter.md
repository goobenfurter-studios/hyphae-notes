# Executive Summary
	- A hypha (pl. hyphae) is the filament a fungus uses to connect to its mycelial network. With this context, [[Hyphae]] aims to provide a [[lang/Nim]] library that allows a user to start their own "mycelial network" within the [[Fediverse]] by implementing [[(streams)]], a federated communications server that uses [[Nomad]]. Specifically, Hyphae allows the user to establish a [[nomadic identity]] that allows them to enter their network from multiple points rather than just one server or domain.
- # Project Scope
	- ## Goals and Objectives
		- Hyphae's primary purpose is to provide a protocol library for [[nomadic identity]] in the [[Fediverse]]. To accomplish this goal, there are several intermediate objectives:
		- Implement the protocols used by [[(streams)]]:
		  logseq.order-list-type:: number
			- [[Nomad]]
			  logseq.order-list-type:: number
	- ## Outcomes and Deliverables
		- A protocol library implementation of [[(streams)]]
		- A test suite for at minimum every call to the API
		- Documentation for both a user and a developer
	- ## Out of Scope
		- A server implementation beyond what is necessary for testing
		- Any extraneous features (those not defined in the protocol)
- # Project Development
	- ## Context
		- ### Explanation of [[ActivityPub]]
			- [[ActivityPub]] is the decentralized social networking protocol that allows the software platforms that make up the [[Fediverse]] to interoperate, broadly speaking. It uses the vocabulary provided by [[ActivityStreams]] 2.0 and is officially published as a W3C recommended standard.
			- [[ActivityPub]] allows for decentralization, but one of its major pain points is that many implementations currently rely on domain-based identities. This means that moving to another server with a different domain name can be technologically challenging. [[Nomad]] is a protocol primarily authored by [[Mike Macgirvin]] that works together with [[ActivityPub]] in order to fix that.
		- ### History of [[Nomad]]
			- One of the earliest precursors of [[Nomad]] is the work [[Mike Macgirvin]] did on DFRN (Distributed Friends and Relations Network) and Friendica. This protocol focused on having an authenticated pipe between two actors in the network and magic-auth. Magic-auth provides cross-site identity and access verification: Alice can log into her own server, which Bob's server then can contact to gives Alice access to Bob's site as Bob has allowed.
			- Then Macgirvin began work on Zot and Hubzilla, which expanded on DFRN but focused less on social networking and more on privacy. Zot solidified magic-auth and provided [[nomadic identity]].
			- His work on nomadic identity is now continued in [[Nomad]] and [[(streams)]], which is what Hyphae is based on.
	- ## Requirements
		- **API Documentation:** The library API should be documented concisely (thoroughly but clearly) for easy implementation in external projects.
		- **Completeness:** The library should implement the complete set of features provided by the protocol.
		- **Ease of Compatibility:** The API should easily bind to whatever interface. For this reason, providing a [[lang/c]] FFI is essential.
		- **Performance:** The library should perform reasonably well in an application. This means being conservative and secure with resources and memory on the machine as well as on the network.
		- **Testing:** The library API should be tested with a suite, not necessarily in a real-world application.
		- **Extensibility:** The library should be modular, making it trivial to extend its capabilities in the future.
	- ## Constraints and Risks
		- There is no time constraint.
		- The project is unfunded and will need to spend only time and no money.
		- No team members have experience implementing network protocols, so we may be greatly underestimating the work involved.
		- There are not many other projects (besides [[(streams)]]) trying to implement these protocols, so our perspective will be very narrow and largely based on the [[(streams)]] project.
	- ## NOW Roadmap
	  :LOGBOOK:
	  CLOCK: [2024-04-04 Thu 20:36:21]--[2024-04-04 Thu 20:36:22] =>  00:00:01
	  CLOCK: [2024-04-04 Thu 20:36:23]
	  :END:
		- DONE Create Github Repo
		- TODO Planning Documentation
		- TODO Diagrams Detailing Developer's Understanding of the Protocol
		- TODO Test Suite Rough Draft
		- TODO FULLY OPERATIONAL~ Test Suite
		- TODO Implement Protocol
		  :LOGBOOK:
		  CLOCK: [2024-04-04 Thu 20:42:51]--[2024-04-04 Thu 20:42:52] =>  00:00:01
		  :END:
		- TODO End to End Tests
	- ## Prototypes
		- The initial prototype will be a proof of concept library implementation that is not necessarily tested in any real-world applications.
- # Team Development
	- ## Mission and Objectives
		- The Hyphae's team mission is to provide another implementation of the [[Nomad]] protocol used by [[(streams)]] as well as
			- practicing test-driven development,
			- writing back end modules,
			- learning back end tooling, and
			- gaining project management experience.
	- ## Membership
		- [[Göbenfurter Studios]] is an independent developer studio founded by [[Cody Frazier]] and [[Evangeline Barruel]]. The purpose of the studio is to be a platform to allow its developers to explore different areas of programming they are interested in.
		- ### Management Roles
			- Project Manager: [[Cody Frazier]] , [[Eva Barruel]]
			- Assistant Project Manager: [[mascot/Göbenfurter]]
			- Liaison: [[Eva Barruel]]
		- ### Technical Roles
			- Software Architect: [[Cody Frazier]]
				- takes care of high-level structure of codebase
			- Software Designer: [[Eva Barruel]]
				- takes care of low-level operations of codebase
	- ## Relationships
		- **[[(streams)]]:** Hyphae is based on this project but has chosen a language other than [[lang/PHP]] for its implementation — [[lang/Nim]].
- # Definitions
-