# ENS
Encrypted Neural Swarm

I want to make my licensing intentions clear as everything that follows modifies my use of the MIT 2.0 license. I want credit for my work. If you use my work, credit me. If you make changes to this and something is the basis of my work, credit me. If you want to use this in your business, contact me for a license. What you can not do is sell my work. You CAN sell YOUR work that is compatible with my work. If you improve something in what I have done, you agree to make the code available Open Source. If you want to use this in a product for sale or state/national defense, contact me for a licensing arrangement.

This IS NOT going to be effective with LLM's. This system is designed for significantly less data than the size of LLM's. I don't have a max size because it dependant on SO many variables. I will instead provide use cases that this system will work with.

This is not an "install it and it will run," type of project. It's about a 90% solution. It will take some work on your part to make the system work.

If you have questions you can contact me. My gmail account is kd5jos@gmail.com. No, I won't rewrite something for YOUR specific needs. I'm posting this to demonstrate what 15 months of unemployment has me creating. Take this code and improve on it.

With all that said, what exactly is an Encrypted Neural Swarm?
ENS provides a privacy-preserving, decentralized, and auditable system for neural network inference and training by combining homomorphic encryption with blockchain-based model state tracking, enabling distributed, fault-tolerant AI computation across untrusted nodes.

What makes this idea unique:
	•	Use of Paillier (not FHE) to offload expensive operations while still protecting input privacy
	•	Tracking only the model weights on a blockchain as the audit/control layer
	•	Using known plaintext weights for secure, decentralized accumulation of encrypted inputs
	•	Creating a system that’s:
	•	Distributed,
	•	Verifiable,
	•	Privacy-preserving,
	•	Modular — nodes can be added/removed, and the blockchain handles continuity

To my knowledge, no academic or industry system has combined these exact primitives using this architectural method.

What exactly does this mean? Well, let me give you some use cases to help you understand what I have created.

Autonomous Systems with Subordinate Agents

Use Case: Central Vehicle + Encrypted Drone Wingmen
	•	Scenario: A central vehicle (e.g., command tank, mothership, rescue leader) dispatches tasks to nearby drones or robots.
	•	Function: Drones process encrypted input (e.g., video, telemetry) using a shared model.
	•	Security: The drones can compute over encrypted data but cannot decrypt it, preserving mission secrecy and isolation.
	•	Value: Even if drones are captured or jammed, they cannot reveal sensitive data or model behavior.

 Medical AI with Patient Data Confidentiality

Use Case: Encrypted Diagnosis Pipeline
	•	Scenario: A patient submits their health data encrypted with their public key.
	•	Function: Hospitals or diagnostic AIs can compute potential diagnoses without ever accessing raw patient data.
	•	Output: The result is returned to the patient (or authorized physician), who decrypts it.
	•	Value: Complete HIPAA-compliant workflows with no centralized data exposure — perfect for federated hospitals or cross-border cases.

 Federated Training with Auditable Integrity

Use Case: Multi-party Model Training
	•	Scenario: A set of institutions (e.g., banks, research labs) collaboratively train a model, but do not trust each other with raw data.
	•	Function: Each party submits encrypted updates; ENS validates updates against a blockchain and applies them homomorphically.
	•	Value: Enables decentralized training without ever pooling raw data, and with on-chain auditability.

 Privacy-Preserving Industrial Edge AI

Use Case: Factory Machines + Central Model
	•	Scenario: Edge devices in a manufacturing plant observe conditions (e.g. temperature, vibration).
	•	Function: Devices encrypt sensor data and send to a local ENS swarm.
	•	Output: Model predicts failure risk, operating thresholds, etc.
	•	Value: No edge device can be compromised to leak trade secrets or proprietary operations.

 Regulated Finance and Credit Scoring

Use Case: Private Credit Models
	•	Scenario: Credit scoring AIs compute predictions on encrypted financial histories.
	•	Value: Lenders never see raw salary, debt, or demographic data — only model outputs and verifiable audit trails.

 Smart Contracts with Off-Chain Intelligence

Use Case: Encrypted AI Oracle
	•	Scenario: A smart contract requests a prediction (e.g. fraud risk, insurance premium).
	•	Function: ENS handles the compute, returning encrypted results back on-chain.
	•	Value: On-chain systems access powerful AI without ever touching sensitive input or model data.

 Defense and National Security
 
Use Case: Secure Joint Intelligence Analysis
 	•	Scenario: Multiple agencies collaborate to analyze satellite or sensor data.
  	•	Function: Each agency provides encrypted features; ENS processes and returns results securely.
   	•	Value: Collaboration without compromising classified datasets or exposing inter-agency logic.

  Routing and Switching
  
Use Case: Privacy-Preserving Network Routing with ENS
	•	Scenario: 
 	Each network node has local information (e.g., bandwidth, latency, congestion)
  	This information is encrypted using a shared Paillier public key
   	Nodes send encrypted metrics to a swarm node (or set of swarm nodes)
    	The swarm performs homomorphic accumulation and comparisons
     	The result helps compute the best next hop, optimal path, or route weights — without any node revealing its actual metrics
      	•	Function:
  	Node A wants to forward a packet
        It sends:
		A request to swarm: “Which neighbor (B, C, D) has best current cost to destination?” along with encrypted costs Enc(cost_B), Enc(cost_C), Enc(cost_D)
        Swarm node performs encrypted comparison logic:
		Could apply pre-trained models or aggregate encrypted cost values from multiple hops
        Swarm returns encrypted ranking or recommendation
	Node A decrypts and selects the best path
 	•	Value:
	Network privacy	 is maintained because costs and paths stay encrypted, there is no central visibility.
        Decentralized path selection because multiple swarm nodes can evaluate options independently.
	Zero trust compliant because nodes don’t need to trust neighbors with raw state.
        Built in real-time adaptability	because the Model Keeper can retrain based on encrypted traffic stats.
	Compliance (e.g. anonymity networks)	through traffic shaping and metrics staying fully private.
 	It’s especially useful in:
  		•	Zero-trust networks (mesh included)
    		•	Overlay routing (e.g. Tor-like anonymity systems)
      		•	Disaster recovery & ad-hoc tactical networks

Obviously this can be a powerful tool for many different uses. These are just examples. I'm the only developer on this project. I don't have a college degree. The work you see here is because of research, trial, and error. I have probably made mistakes. There is no warranty AT ALL, in ANYTHING I provide. You use this code/architecture at your own risk.
