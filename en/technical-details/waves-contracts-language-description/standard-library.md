# Standard Library

# Types
|type|adds|
|-------|---|
| [Unit](#Unit) | Native |   
| [Int](#Int) | Native |   
| [Boolean](#Boolean) | Native |   
| [ByteVector](#ByteVector) | Native |   
| [String](#String) | Native |   
| [Address](#Address) |   <ul> <li> **bytes**  [ByteVector](#ByteVector) </li></ul>| 
| [Alias](#Alias) |   <ul> <li> **alias**  [String](#String) </li></ul>| 
| [Transfer](#Transfer) |   <ul> <li> **recipient** [Address](#Address) [Alias](#Alias) </li> <li> **amount**  [Int](#Int) </li></ul>| 
| [Order](#Order) |   <ul> <li> **id**  [ByteVector](#ByteVector) </li> <li> **matcherPublicKey**  [ByteVector](#ByteVector) </li> <li> **assetPair** [AssetPair](#AssetPair) </li> <li> **orderType** [Buy](#Buy) [Sell](#Sell) </li> <li> **price**  [Int](#Int) </li> <li> **amount**  [Int](#Int) </li> <li> **timestamp**  [Int](#Int) </li> <li> **expiration**  [Int](#Int) </li> <li> **matcherFee**  [Int](#Int) </li> <li> **sender** [Address](#Address) </li> <li> **senderPublicKey**  [ByteVector](#ByteVector) </li> <li> **bodyBytes**  [ByteVector](#ByteVector) </li> <li> **proofs**  [LIST](#LIST)[ [ByteVector](#ByteVector)]</li></ul>| 
| [AssetPair](#AssetPair) |   <ul> <li> **amountAsset**  [OPTION](#OPTION)[ [ByteVector](#ByteVector)]</li> <li> **priceAsset**  [OPTION](#OPTION)[ [ByteVector](#ByteVector)]</li></ul>| 
| [DataEntry](#DataEntry) |   <ul> <li> **key**  [String](#String) </li> <li> **value** [Int](#Int) [Boolean](#Boolean) [ByteVector](#ByteVector) [String](#String) </li></ul>| 
| [Transaction](#Transaction) |    [TransferTransaction](#TransferTransaction) [IssueTransaction](#IssueTransaction) [ReissueTransaction](#ReissueTransaction) [BurnTransaction](#BurnTransaction) [LeaseTransaction](#LeaseTransaction) [LeaseCancelTransaction](#LeaseCancelTransaction) [MassTransferTransaction](#MassTransferTransaction) [CreateAliasTransaction](#CreateAliasTransaction) [SetScriptTransaction](#SetScriptTransaction) [SponsorFeeTransaction](#SponsorFeeTransaction) [ExchangeTransaction](#ExchangeTransaction) [DataTransaction](#DataTransaction)
| [GenesisTransaction](#GenesisTransaction) |   <ul> <li> **amount**  [Int](#Int) </li> <li> **recipient** [Address](#Address) [Alias](#Alias) </li> <li> **id**  [ByteVector](#ByteVector) </li> <li> **fee**  [Int](#Int) </li> <li> **timestamp**  [Int](#Int) </li> <li> **version**  [Int](#Int) </li></ul>| 
| [PaymentTransaction](#PaymentTransaction) |   <ul> <li> **amount**  [Int](#Int) </li> <li> **recipient** [Address](#Address) [Alias](#Alias) </li> <li> **id**  [ByteVector](#ByteVector) </li> <li> **fee**  [Int](#Int) </li> <li> **timestamp**  [Int](#Int) </li> <li> **version**  [Int](#Int) </li> <li> **sender** [Address](#Address) </li> <li> **senderPublicKey**  [ByteVector](#ByteVector) </li> <li> **bodyBytes**  [ByteVector](#ByteVector) </li> <li> **proofs**  [LIST](#LIST)[ [ByteVector](#ByteVector)]</li></ul>| 
| [TransferTransaction](#TransferTransaction) |   <ul> <li> **feeAssetId**  [OPTION](#OPTION)[ [ByteVector](#ByteVector)]</li> <li> **amount**  [Int](#Int) </li> <li> **assetId**  [OPTION](#OPTION)[ [ByteVector](#ByteVector)]</li> <li> **recipient** [Address](#Address) [Alias](#Alias) </li> <li> **attachment**  [ByteVector](#ByteVector) </li> <li> **id**  [ByteVector](#ByteVector) </li> <li> **fee**  [Int](#Int) </li> <li> **timestamp**  [Int](#Int) </li> <li> **version**  [Int](#Int) </li> <li> **sender** [Address](#Address) </li> <li> **senderPublicKey**  [ByteVector](#ByteVector) </li> <li> **bodyBytes**  [ByteVector](#ByteVector) </li> <li> **proofs**  [LIST](#LIST)[ [ByteVector](#ByteVector)]</li></ul>| 
| [IssueTransaction](#IssueTransaction) |   <ul> <li> **quantity**  [Int](#Int) </li> <li> **name**  [ByteVector](#ByteVector) </li> <li> **description**  [ByteVector](#ByteVector) </li> <li> **reissuable**  [Boolean](#Boolean) </li> <li> **decimals**  [Int](#Int) </li> <li> **script**  [OPTION](#OPTION)[ [ByteVector](#ByteVector)]</li> <li> **id**  [ByteVector](#ByteVector) </li> <li> **fee**  [Int](#Int) </li> <li> **timestamp**  [Int](#Int) </li> <li> **version**  [Int](#Int) </li> <li> **sender** [Address](#Address) </li> <li> **senderPublicKey**  [ByteVector](#ByteVector) </li> <li> **bodyBytes**  [ByteVector](#ByteVector) </li> <li> **proofs**  [LIST](#LIST)[ [ByteVector](#ByteVector)]</li></ul>| 
| [ReissueTransaction](#ReissueTransaction) |   <ul> <li> **quantity**  [Int](#Int) </li> <li> **assetId**  [ByteVector](#ByteVector) </li> <li> **reissuable**  [Boolean](#Boolean) </li> <li> **id**  [ByteVector](#ByteVector) </li> <li> **fee**  [Int](#Int) </li> <li> **timestamp**  [Int](#Int) </li> <li> **version**  [Int](#Int) </li> <li> **sender** [Address](#Address) </li> <li> **senderPublicKey**  [ByteVector](#ByteVector) </li> <li> **bodyBytes**  [ByteVector](#ByteVector) </li> <li> **proofs**  [LIST](#LIST)[ [ByteVector](#ByteVector)]</li></ul>| 
| [BurnTransaction](#BurnTransaction) |   <ul> <li> **quantity**  [Int](#Int) </li> <li> **assetId**  [ByteVector](#ByteVector) </li> <li> **id**  [ByteVector](#ByteVector) </li> <li> **fee**  [Int](#Int) </li> <li> **timestamp**  [Int](#Int) </li> <li> **version**  [Int](#Int) </li> <li> **sender** [Address](#Address) </li> <li> **senderPublicKey**  [ByteVector](#ByteVector) </li> <li> **bodyBytes**  [ByteVector](#ByteVector) </li> <li> **proofs**  [LIST](#LIST)[ [ByteVector](#ByteVector)]</li></ul>| 
| [LeaseTransaction](#LeaseTransaction) |   <ul> <li> **amount**  [Int](#Int) </li> <li> **recipient** [Address](#Address) [Alias](#Alias) </li> <li> **id**  [ByteVector](#ByteVector) </li> <li> **fee**  [Int](#Int) </li> <li> **timestamp**  [Int](#Int) </li> <li> **version**  [Int](#Int) </li> <li> **sender** [Address](#Address) </li> <li> **senderPublicKey**  [ByteVector](#ByteVector) </li> <li> **bodyBytes**  [ByteVector](#ByteVector) </li> <li> **proofs**  [LIST](#LIST)[ [ByteVector](#ByteVector)]</li></ul>| 
| [LeaseCancelTransaction](#LeaseCancelTransaction) |   <ul> <li> **leaseId**  [ByteVector](#ByteVector) </li> <li> **id**  [ByteVector](#ByteVector) </li> <li> **fee**  [Int](#Int) </li> <li> **timestamp**  [Int](#Int) </li> <li> **version**  [Int](#Int) </li> <li> **sender** [Address](#Address) </li> <li> **senderPublicKey**  [ByteVector](#ByteVector) </li> <li> **bodyBytes**  [ByteVector](#ByteVector) </li> <li> **proofs**  [LIST](#LIST)[ [ByteVector](#ByteVector)]</li></ul>| 
| [MassTransferTransaction](#MassTransferTransaction) |   <ul> <li> **feeAssetId**  [OPTION](#OPTION)[ [ByteVector](#ByteVector)]</li> <li> **assetId**  [OPTION](#OPTION)[ [ByteVector](#ByteVector)]</li> <li> **totalAmount**  [Int](#Int) </li> <li> **transfers**  [LIST](#LIST)[ [Transfer](#Transfer)]</li> <li> **transferCount**  [Int](#Int) </li> <li> **attachment**  [ByteVector](#ByteVector) </li> <li> **id**  [ByteVector](#ByteVector) </li> <li> **fee**  [Int](#Int) </li> <li> **timestamp**  [Int](#Int) </li> <li> **version**  [Int](#Int) </li> <li> **sender** [Address](#Address) </li> <li> **senderPublicKey**  [ByteVector](#ByteVector) </li> <li> **bodyBytes**  [ByteVector](#ByteVector) </li> <li> **proofs**  [LIST](#LIST)[ [ByteVector](#ByteVector)]</li></ul>| 
| [CreateAliasTransaction](#CreateAliasTransaction) |   <ul> <li> **alias**  [String](#String) </li> <li> **id**  [ByteVector](#ByteVector) </li> <li> **fee**  [Int](#Int) </li> <li> **timestamp**  [Int](#Int) </li> <li> **version**  [Int](#Int) </li> <li> **sender** [Address](#Address) </li> <li> **senderPublicKey**  [ByteVector](#ByteVector) </li> <li> **bodyBytes**  [ByteVector](#ByteVector) </li> <li> **proofs**  [LIST](#LIST)[ [ByteVector](#ByteVector)]</li></ul>| 
| [SetScriptTransaction](#SetScriptTransaction) |   <ul> <li> **script**  [OPTION](#OPTION)[ [ByteVector](#ByteVector)]</li> <li> **id**  [ByteVector](#ByteVector) </li> <li> **fee**  [Int](#Int) </li> <li> **timestamp**  [Int](#Int) </li> <li> **version**  [Int](#Int) </li> <li> **sender** [Address](#Address) </li> <li> **senderPublicKey**  [ByteVector](#ByteVector) </li> <li> **bodyBytes**  [ByteVector](#ByteVector) </li> <li> **proofs**  [LIST](#LIST)[ [ByteVector](#ByteVector)]</li></ul>| 
| [SponsorFeeTransaction](#SponsorFeeTransaction) |   <ul> <li> **assetId**  [ByteVector](#ByteVector) </li> <li> **minSponsoredAssetFee**  [OPTION](#OPTION)[ [Int](#Int)]</li> <li> **id**  [ByteVector](#ByteVector) </li> <li> **fee**  [Int](#Int) </li> <li> **timestamp**  [Int](#Int) </li> <li> **version**  [Int](#Int) </li> <li> **sender** [Address](#Address) </li> <li> **senderPublicKey**  [ByteVector](#ByteVector) </li> <li> **bodyBytes**  [ByteVector](#ByteVector) </li> <li> **proofs**  [LIST](#LIST)[ [ByteVector](#ByteVector)]</li></ul>| 
| [ExchangeTransaction](#ExchangeTransaction) |   <ul> <li> **buyOrder** [Order](#Order) </li> <li> **sellOrder** [Order](#Order) </li> <li> **price**  [Int](#Int) </li> <li> **amount**  [Int](#Int) </li> <li> **buyMatcherFee**  [Int](#Int) </li> <li> **sellMatcherFee**  [Int](#Int) </li> <li> **id**  [ByteVector](#ByteVector) </li> <li> **fee**  [Int](#Int) </li> <li> **timestamp**  [Int](#Int) </li> <li> **version**  [Int](#Int) </li> <li> **sender** [Address](#Address) </li> <li> **senderPublicKey**  [ByteVector](#ByteVector) </li> <li> **bodyBytes**  [ByteVector](#ByteVector) </li> <li> **proofs**  [LIST](#LIST)[ [ByteVector](#ByteVector)]</li></ul>| 
| [DataTransaction](#DataTransaction) |   <ul> <li> **data**  [LIST](#LIST)[ [DataEntry](#DataEntry)]</li> <li> **id**  [ByteVector](#ByteVector) </li> <li> **fee**  [Int](#Int) </li> <li> **timestamp**  [Int](#Int) </li> <li> **version**  [Int](#Int) </li> <li> **sender** [Address](#Address) </li> <li> **senderPublicKey**  [ByteVector](#ByteVector) </li> <li> **bodyBytes**  [ByteVector](#ByteVector) </li> <li> **proofs**  [LIST](#LIST)[ [ByteVector](#ByteVector)]</li></ul>| 

# Input variables
|vars|type|doc|
|-------|---|---|
| unit| [Unit](#Unit) | Single instance value|
| height| [Int](#Int) | Current blockchain height|
| tx| [Order](#Order) [TransferTransaction](#TransferTransaction) [IssueTransaction](#IssueTransaction) [ReissueTransaction](#ReissueTransaction) [BurnTransaction](#BurnTransaction) [LeaseTransaction](#LeaseTransaction) [LeaseCancelTransaction](#LeaseCancelTransaction) [MassTransferTransaction](#MassTransferTransaction) [CreateAliasTransaction](#CreateAliasTransaction) [SetScriptTransaction](#SetScriptTransaction) [SponsorFeeTransaction](#SponsorFeeTransaction) [ExchangeTransaction](#ExchangeTransaction) [DataTransaction](#DataTransaction)|  Processing transaction|


# Functions
|funcs|cost|doc|params|type|
|-------|-|---|---|---|
| fraction|1|Multiply and dividion with big integer intermediate representation|<ul> <li>value [Int](#Int) multiplyer</li> <li>numerator [Int](#Int) multiplyer</li> <li>denominator [Int](#Int) divisor</li></ul>| [Int](#Int)
| size|1|Size of bytes vector|<ul> <li>byteVector [ByteVector](#ByteVector) vector</li></ul>| [Int](#Int)
| toBytes|1|Bytes array representation|<ul> <li>b [Boolean](#Boolean) value</li></ul>| [ByteVector](#ByteVector)
| toBytes|1|Bytes array representation|<ul> <li>n [Int](#Int) value</li></ul>| [ByteVector](#ByteVector)
| toBytes|1|Bytes array representation|<ul> <li>s [String](#String) value</li></ul>| [ByteVector](#ByteVector)
| take|1|Take firsts bytes subvector|<ul> <li>xs [ByteVector](#ByteVector) vector</li> <li>number [Int](#Int) Bytes number</li></ul>| [ByteVector](#ByteVector)
| drop|1|Skip firsts bytes|<ul> <li>xs [ByteVector](#ByteVector) vector</li> <li>number [Int](#Int) Bytes number</li></ul>| [ByteVector](#ByteVector)
| takeRight||Take vector tail|<ul> <li>@xs [ByteVector](#ByteVector) vector</li> <li>@number [Int](#Int) taking size</li></ul>| [ByteVector](#ByteVector)
| dropRight||Cut vectors tail|<ul> <li>@xs [ByteVector](#ByteVector) vector</li> <li>@number [Int](#Int) cuting size</li></ul>| [ByteVector](#ByteVector)
| size|1|Scting size in characters|<ul> <li>xs [String](#String) string</li></ul>| [Int](#Int)
| toString|1|String representation|<ul> <li>b [Boolean](#Boolean) value</li></ul>| [String](#String)
| toString|1|String representation|<ul> <li>n [Int](#Int) value</li></ul>| [String](#String)
| take|1|Take string prefix|<ul> <li>xs [String](#String) sctring</li> <li>number [Int](#Int) prefix size in characters</li></ul>| [String](#String)
| drop|1|Remmove sring prefix|<ul> <li>xs [String](#String) string</li> <li>number [Int](#Int) prefix size</li></ul>| [String](#String)
| takeRight||Take string suffix|<ul> <li>@xs [String](#String) String</li> <li>@number [Int](#Int) suffix size in characters</li></ul>| [String](#String)
| dropRight||Remove string suffix|<ul> <li>@xs [String](#String) string</li> <li>@number [Int](#Int) suffix size in characters</li></ul>| [String](#String)
| _isInstanceOf|1|Internal function to check value type|<ul> <li>obj T value</li> <li>of [String](#String) type name</li></ul>| [Boolean](#Boolean)
| isDefined||Check the value is defined|<ul> <li>@a OPTION[ T] Option value</li></ul>| [Boolean](#Boolean)
| extract||Extract value from option or fail|<ul> <li>@a OPTION[ T] Optional value</li></ul>|  T
| throw|1|Fail script|<ul> <li>err [String](#String) Error message</li></ul>| [Nothing](#Nothing)
| throw||Fail script|<ul></ul>| [Nothing](#Nothing)
| *|1|Integer multiplication|<ul> <li>a [Int](#Int) multiplyer</li> <li>b [Int](#Int) multiplyer</li></ul>| [Int](#Int)
| /|1|Integer devision|<ul> <li>a [Int](#Int) divisible</li> <li>b [Int](#Int) divisor</li></ul>| [Int](#Int)
| %|1|Modulo|<ul> <li>a [Int](#Int) divisible</li> <li>b [Int](#Int) divisor</li></ul>| [Int](#Int)
| +|1|Integer sum|<ul> <li>a [Int](#Int) term</li> <li>b [Int](#Int) term</li></ul>| [Int](#Int)
| -|1|Integer substitution|<ul> <li>a [Int](#Int) term</li> <li>b [Int](#Int) term</li></ul>| [Int](#Int)
| +|10|Limited strings concatination|<ul> <li>a [String](#String) prefix</li> <li>b [String](#String) suffix</li></ul>| [String](#String)
| +|10|Limited bytes vectors concatination|<ul> <li>a [ByteVector](#ByteVector) prefix</li> <li>b [ByteVector](#ByteVector) suffix</li></ul>| [ByteVector](#ByteVector)
| &#61;&#61;|1|Equality|<ul> <li>a T value</li> <li>b T value</li></ul>| [Boolean](#Boolean)
| !&#61;||Inequality|<ul> <li>@a T value</li> <li>@b T value</li></ul>| [Boolean](#Boolean)
| &gt;&#61;|1|Integer grater or equal comparation|<ul> <li>a [Int](#Int) term</li> <li>b [Int](#Int) term</li></ul>| [Boolean](#Boolean)
| &gt;|1|Integer grater comparation|<ul> <li>a [Int](#Int) term</li> <li>b [Int](#Int) term</li></ul>| [Boolean](#Boolean)
| getElement|2|Get list element by position|<ul> <li>arr LIST[ T] list</li> <li>pos [Int](#Int) element position</li></ul>|  T
| size|2|Size of list|<ul> <li>arr LIST[ T] list</li></ul>| [Int](#Int)
| -||Change integer sign|<ul> <li>@n [Int](#Int) value</li></ul>| [Int](#Int)
| !||unary negation|<ul> <li>@p [Boolean](#Boolean) boolean</li></ul>| [Boolean](#Boolean)
| keccak256|10|256 bit Keccak/SHA-3/TIPS-202|<ul> <li>bytes [ByteVector](#ByteVector) value</li></ul>| [ByteVector](#ByteVector)
| blake2b256|10|256 bit BLAKE|<ul> <li>bytes [ByteVector](#ByteVector) value</li></ul>| [ByteVector](#ByteVector)
| sha256|10|256 bit SHA-2|<ul> <li>bytes [ByteVector](#ByteVector) value</li></ul>| [ByteVector](#ByteVector)
| sigVerify|100|check signature|<ul> <li>message [ByteVector](#ByteVector) value</li> <li>sig [ByteVector](#ByteVector) signature</li> <li>pub [ByteVector](#ByteVector) public key</li></ul>| [Boolean](#Boolean)
| toBase58String|10|Base58 encode|<ul> <li>bytes [ByteVector](#ByteVector) value</li></ul>| [String](#String)
| fromBase58String|10|Base58 decode|<ul> <li>str [String](#String) base58 encoded string</li></ul>| [ByteVector](#ByteVector)
| toBase64String|10|Base64 encode|<ul> <li>bytes [ByteVector](#ByteVector) value</li></ul>| [String](#String)
| fromBase64String|10|Base64 decode|<ul> <li>str [String](#String) base64 encoded string</li></ul>| [ByteVector](#ByteVector)
| transactionById|100|Lookup transaction|<ul> <li>id [ByteVector](#ByteVector) transaction Id</li></ul>| [Unit](#Unit) [GenesisTransaction](#GenesisTransaction) [PaymentTransaction](#PaymentTransaction) [TransferTransaction](#TransferTransaction) [IssueTransaction](#IssueTransaction) [ReissueTransaction](#ReissueTransaction) [BurnTransaction](#BurnTransaction) [LeaseTransaction](#LeaseTransaction) [LeaseCancelTransaction](#LeaseCancelTransaction) [MassTransferTransaction](#MassTransferTransaction) [CreateAliasTransaction](#CreateAliasTransaction) [SetScriptTransaction](#SetScriptTransaction) [SponsorFeeTransaction](#SponsorFeeTransaction) [ExchangeTransaction](#ExchangeTransaction) [DataTransaction](#DataTransaction)
| transactionHeightById|100|get height when transaction was stored to blockchain|<ul> <li>id [ByteVector](#ByteVector) transaction Id</li></ul>| OPTION[ [Int](#Int)] 
| getInteger|100|get data from the account state|<ul> <li>addressOrAlias [Address](#Address) [Alias](#Alias) account</li> <li>key [String](#String) key</li></ul>| OPTION[ [Int](#Int)] 
| getBoolean|100|get data from the account state|<ul> <li>addressOrAlias [Address](#Address) [Alias](#Alias) account</li> <li>key [String](#String) key</li></ul>| OPTION[ [Boolean](#Boolean)] 
| getBinary|100|get data from the account state|<ul> <li>addressOrAlias [Address](#Address) [Alias](#Alias) account</li> <li>key [String](#String) key</li></ul>| OPTION[ [ByteVector](#ByteVector)] 
| getString|100|get data from the account state|<ul> <li>addressOrAlias [Address](#Address) [Alias](#Alias) account</li> <li>key [String](#String) key</li></ul>| OPTION[ [String](#String)] 
| getInteger|10|Find and extract data by key|<ul> <li>data LIST[ [DataEntry](#DataEntry)] DataEntry vector, usally tx.data</li> <li>key [String](#String) key</li></ul>| OPTION[ [Int](#Int)] 
| getBoolean|10|Find and extract data by key|<ul> <li>data LIST[ [DataEntry](#DataEntry)] DataEntry vector, usally tx.data</li> <li>key [String](#String) key</li></ul>| OPTION[ [Boolean](#Boolean)] 
| getBinary|10|Find and extract data by key|<ul> <li>data LIST[ [DataEntry](#DataEntry)] DataEntry vector, usally tx.data</li> <li>key [String](#String) key</li></ul>| OPTION[ [ByteVector](#ByteVector)] 
| getString|10|Find and extract data by key|<ul> <li>data LIST[ [DataEntry](#DataEntry)] DataEntry vector, usally tx.data</li> <li>key [String](#String) key</li></ul>| OPTION[ [String](#String)] 
| getInteger||Extract data by index|<ul> <li>@data LIST[ [DataEntry](#DataEntry)] DataEntry vector, usally tx.data</li> <li>@index [Int](#Int) index</li></ul>| OPTION[ [Int](#Int)] 
| getBoolean||Extract data by index|<ul> <li>@data LIST[ [DataEntry](#DataEntry)] DataEntry vector, usally tx.data</li> <li>@index [Int](#Int) index</li></ul>| OPTION[ [Boolean](#Boolean)] 
| getBinary||Extract data by index|<ul> <li>@data LIST[ [DataEntry](#DataEntry)] DataEntry vector, usally tx.data</li> <li>@index [Int](#Int) index</li></ul>| OPTION[ [ByteVector](#ByteVector)] 
| getString||Extract data by index|<ul> <li>@data LIST[ [DataEntry](#DataEntry)] DataEntry vector, usally tx.data</li> <li>@index [Int](#Int) index</li></ul>| OPTION[ [String](#String)] 
| addressFromPublicKey||Convert public key to account address|<ul> <li>@publicKey [ByteVector](#ByteVector) public key</li></ul>| [Address](#Address)
| addressFromString||Decode account address|<ul> <li>@string [String](#String) string address represntation</li></ul>| OPTION[ [Address](#Address)] 
| addressFromRecipient|100|Extract address or lookup alias|<ul> <li>AddressOrAlias [Address](#Address) [Alias](#Alias) address or alias, usually tx.recipient</li></ul>| [Address](#Address)
| assetBalance|100|get asset balance for account|<ul> <li>addressOrAlias [Address](#Address) [Alias](#Alias) account</li> <li>assetId OPTION[ [ByteVector](#ByteVector)] assetId (WAVES if none)</li></ul>| [Int](#Int)
| wavesBalance||get WAVES balanse for account|<ul> <li>@addressOrAlias [Address](#Address) [Alias](#Alias) account</li></ul>| [Int](#Int)


# Common fields
|tx type|id | fee| timestamp|version|sender|senderPublicKey|bodyBytes|proofs|
|---|---|---|---|---|---|---|---|---|
|TransferTransaction|  [ByteVector](#ByteVector) |  [Int](#Int) |  [Int](#Int) |  [Int](#Int) |  [Address](#Address) |  [ByteVector](#ByteVector) |  [ByteVector](#ByteVector) |  LIST[[ByteVector](#ByteVector)]|
|IssueTransaction|  [ByteVector](#ByteVector) |  [Int](#Int) |  [Int](#Int) |  [Int](#Int) |  [Address](#Address) |  [ByteVector](#ByteVector) |  [ByteVector](#ByteVector) |  LIST[[ByteVector](#ByteVector)]|
|ReissueTransaction|  [ByteVector](#ByteVector) |  [Int](#Int) |  [Int](#Int) |  [Int](#Int) |  [Address](#Address) |  [ByteVector](#ByteVector) |  [ByteVector](#ByteVector) |  LIST[[ByteVector](#ByteVector)]|
|BurnTransaction|  [ByteVector](#ByteVector) |  [Int](#Int) |  [Int](#Int) |  [Int](#Int) |  [Address](#Address) |  [ByteVector](#ByteVector) |  [ByteVector](#ByteVector) |  LIST[[ByteVector](#ByteVector)]|
|LeaseTransaction|  [ByteVector](#ByteVector) |  [Int](#Int) |  [Int](#Int) |  [Int](#Int) |  [Address](#Address) |  [ByteVector](#ByteVector) |  [ByteVector](#ByteVector) |  LIST[[ByteVector](#ByteVector)]|
|LeaseCancelTransaction|  [ByteVector](#ByteVector) |  [Int](#Int) |  [Int](#Int) |  [Int](#Int) |  [Address](#Address) |  [ByteVector](#ByteVector) |  [ByteVector](#ByteVector) |  LIST[[ByteVector](#ByteVector)]|
|MassTransferTransaction|  [ByteVector](#ByteVector) |  [Int](#Int) |  [Int](#Int) |  [Int](#Int) |  [Address](#Address) |  [ByteVector](#ByteVector) |  [ByteVector](#ByteVector) |  LIST[[ByteVector](#ByteVector)]|
|CreateAliasTransaction|  [ByteVector](#ByteVector) |  [Int](#Int) |  [Int](#Int) |  [Int](#Int) |  [Address](#Address) |  [ByteVector](#ByteVector) |  [ByteVector](#ByteVector) |  LIST[[ByteVector](#ByteVector)]|
|SetScriptTransaction|  [ByteVector](#ByteVector) |  [Int](#Int) |  [Int](#Int) |  [Int](#Int) |  [Address](#Address) |  [ByteVector](#ByteVector) |  [ByteVector](#ByteVector) |  LIST[[ByteVector](#ByteVector)]|
|SponsorFeeTransaction|  [ByteVector](#ByteVector) |  [Int](#Int) |  [Int](#Int) |  [Int](#Int) |  [Address](#Address) |  [ByteVector](#ByteVector) |  [ByteVector](#ByteVector) |  LIST[[ByteVector](#ByteVector)]|
|ExchangeTransaction|  [ByteVector](#ByteVector) |  [Int](#Int) |  [Int](#Int) |  [Int](#Int) |  [Address](#Address) |  [ByteVector](#ByteVector) |  [ByteVector](#ByteVector) |  LIST[[ByteVector](#ByteVector)]|
|DataTransaction|  [ByteVector](#ByteVector) |  [Int](#Int) |  [Int](#Int) |  [Int](#Int) |  [Address](#Address) |  [ByteVector](#ByteVector) |  [ByteVector](#ByteVector) |  LIST[[ByteVector](#ByteVector)]|


 <h1>Transfers fields</h1><table><tr><td></td><td>PaymentTransaction</td><td>TransferTransaction</td><td>MassTransferTransaction</td><tr><tr><td>amount</td><td>  <a href="#Int">Int</a></td><td>  <a href="#Int">Int</a></td><td>-</td></tr><tr><td>recipient</td><td>    <a href="#Address">Address</a> <a href="#Alias">Alias</a></td><td>    <a href="#Address">Address</a> <a href="#Alias">Alias</a></td><td>-</td></tr><tr><td>feeAssetId</td><td>-</td><td>  OPTION[<a href="#ByteVector">ByteVector</a>]</td><td>  OPTION[<a href="#ByteVector">ByteVector</a>]</td></tr><tr><td>assetId</td><td>-</td><td>  OPTION[<a href="#ByteVector">ByteVector</a>]</td><td>  OPTION[<a href="#ByteVector">ByteVector</a>]</td></tr><tr><td>attachment</td><td>-</td><td>  <a href="#ByteVector">ByteVector</a></td><td>  <a href="#ByteVector">ByteVector</a></td></tr><tr><td>totalAmount</td><td>-</td><td>-</td><td>  <a href="#Int">Int</a></td></tr><tr><td>transfers</td><td>-</td><td>-</td><td>  LIST[<a href="#Transfer">Transfer</a>]</td></tr><tr><td>transferCount</td><td>-</td><td>-</td><td>  <a href="#Int">Int</a></td></tr></table>

 <h1>Issuing assets fields</h1><table><tr><td></td><td>IssueTransaction</td><td>ReissueTransaction</td><td>BurnTransaction</td><td>SponsorFeeTransaction</td><tr><tr><td>quantity</td><td>  <a href="#Int">Int</a></td><td>  <a href="#Int">Int</a></td><td>  <a href="#Int">Int</a></td><td>-</td></tr><tr><td>name</td><td>  <a href="#ByteVector">ByteVector</a></td><td>-</td><td>-</td><td>-</td></tr><tr><td>description</td><td>  <a href="#ByteVector">ByteVector</a></td><td>-</td><td>-</td><td>-</td></tr><tr><td>reissuable</td><td>  <a href="#Boolean">Boolean</a></td><td>  <a href="#Boolean">Boolean</a></td><td>-</td><td>-</td></tr><tr><td>decimals</td><td>  <a href="#Int">Int</a></td><td>-</td><td>-</td><td>-</td></tr><tr><td>script</td><td>  OPTION[<a href="#ByteVector">ByteVector</a>]</td><td>-</td><td>-</td><td>-</td></tr><tr><td>assetId</td><td>-</td><td>  <a href="#ByteVector">ByteVector</a></td><td>  <a href="#ByteVector">ByteVector</a></td><td>  <a href="#ByteVector">ByteVector</a></td></tr><tr><td>minSponsoredAssetFee</td><td>-</td><td>-</td><td>-</td><td>  OPTION[<a href="#Int">Int</a>]</td></tr></table>

 <h1>Leasing fields</h1><table><tr><td></td><td>LeaseTransaction</td><td>LeaseCancelTransaction</td><tr><tr><td>amount</td><td>  <a href="#Int">Int</a></td><td>-</td></tr><tr><td>recipient</td><td>    <a href="#Address">Address</a> <a href="#Alias">Alias</a></td><td>-</td></tr><tr><td>leaseId</td><td>-</td><td>  <a href="#ByteVector">ByteVector</a></td></tr></table>

 <h1>Other fields</h1><table><tr><td></td><td>CreateAliasTransaction</td><td>SetScriptTransaction</td><td>ExchangeTransaction</td><td>DataTransaction</td><tr><tr><td>alias</td><td>  <a href="#String">String</a></td><td>-</td><td>-</td><td>-</td></tr><tr><td>script</td><td>-</td><td>  OPTION[<a href="#ByteVector">ByteVector</a>]</td><td>-</td><td>-</td></tr><tr><td>buyOrder</td><td>-</td><td>-</td><td>  <a href="#Order">Order</a></td><td>-</td></tr><tr><td>sellOrder</td><td>-</td><td>-</td><td>  <a href="#Order">Order</a></td><td>-</td></tr><tr><td>price</td><td>-</td><td>-</td><td>  <a href="#Int">Int</a></td><td>-</td></tr><tr><td>amount</td><td>-</td><td>-</td><td>  <a href="#Int">Int</a></td><td>-</td></tr><tr><td>buyMatcherFee</td><td>-</td><td>-</td><td>  <a href="#Int">Int</a></td><td>-</td></tr><tr><td>sellMatcherFee</td><td>-</td><td>-</td><td>  <a href="#Int">Int</a></td><td>-</td></tr><tr><td>data</td><td>-</td><td>-</td><td>-</td><td>  LIST[<a href="#DataEntry">DataEntry</a>]</td></tr></table>


