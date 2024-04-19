alias:: protocol/Nomad

- a [[WebMTA]] that provides a decentralized identity and [communications protocol](https://codeberg.org/streams/streams/src/branch/release/spec/Nomad/Home.md) using HTTPS/JSON
- {{renderer code_diagram, plantuml}}
	- ```plantuml
	  @startuml
	  class Identity {
	  	claim : String
	  	key : String
	  }
	  note right of Identity::key
	  	RSA based
	  end note
	  @enduml
	  ```
-