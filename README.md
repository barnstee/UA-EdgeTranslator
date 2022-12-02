# UA Edge Translator
An industrial connectivity edge application translating from proprietary protocols to [OPC UA](https://opcfoundation.org/) leveraging the [W3C Web of Things (WoT)](https://www.w3.org/WoT/) thing descriptions. Thing descriptions can be easily edited using the [Eclipse Foundation's edi{TD}or](https://eclipse.github.io/editdor/).

## How it works

UA Edge Translator solves the common "brownfield" use case of connecting disparate industrial assets with proprietary interfaces and translates their data into an OPC UA information model, enabling processing the assets data either on the edge or in the cloud leveraging a normalized, IEC standard (OPC UA) data format. This accelerates Industrial IoT projects and saves cost since the data doesn't need to be nromalized in the cloud and makes use of the OT expertize foten only found on-premises. For defining a mapping from the proprietary data format to OPC UA, the Web of Things (WoT) "Thing Description" schema is used. Additionally, the mechanism to provide the schema to the Ua Edge Translator is also OPC UA, so for the first time, OPC UA is used for both the control and data plane in this architecture.

## Installation

UA Edge Translator is available as a pre-built Docker cotainer and will run on any Docker- or Kunbernetes-enabled edge device. See "packages" in this repo for details.

## Operation

UA Edge Translator can be controlled through the use of just 3 OPC UA methods reaily available through the OPC UA server interface built in. The methods are:

* CreateAsset(thingDescription) - creates a new asset, returning the ID of the newly created asset on success
* DeleteAsset(assetID) - deletes an asset
* GetAssets() - returns a list of configured assets, each element in the list is a WoT Thing Description
