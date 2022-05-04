0x4742010dbfe107da

# 01 - Chapter 1 Quests

<img src="https://as1.ftcdn.net/v2/jpg/02/83/81/72/1000_F_283817284_g8AT1pMu25kbJvwekoPpFcytCIYiZtp5.jpg" alt="something magnificent" width="600"/>

## Chapter 1 Day 1

### CH1D1 Quest 1: Explain what the Blockchain is in your own words
Blockchain is an open, decentralized network that copy pasta data with each other and verify whether the data and changes to the data are correct. It's open in the sense that anyone is able to read the data stored on the blockchain.

### CH1D1 Quest 2: Explain what a Smart Contract is
Smart Contracts are a way to store code on the blockchain and consists of functions used to interact with the code.

### CH1D1 Quest 3: Explain the difference between a script and a transaction
Scripts are used to read data from a smart contract on the Flow Blockchain. Read-only. Does not require gas fees.
Transactions are used to call functions from a smart contract which change data on the blockchain. Transactions require paying for gas fees.

## Chapter 1 Day 2

### CH1D2 Quest 1: What are the 5 Cadence Programming Language Pillars?
1. Safety and Security
2. Clarity
3. Approachability
4. Developer Experience
5. Resource Oriented Programming

<img src="https://c.tenor.com/vC91HhMF270AAAAM/terio-um.gif" alt="nervous kid" width="300"/>

### CH1D2 Quest 2: In your opinion, even without knowing anything about the Blockchain or coding, why could the 5 Pillars be useful (you don't have to answer this for #5)?

1. Safety and Security: We want to prevent exploits in our contracts and thereby securing our digital assets.
2. Clarity: Explicit design and readability allows for efficient reviewing of smart contract code which give the benefits of development speed and cost-savings.
3. Approachability: By having simple syntax and semantics it becomes easy for developers to get started on a new language such as Cadence quickly.
4. Developer Experience: Great dev tools helps speed up the development process and help making sure that the code works as intended. This leads to more blockchain applications being launched fast.
5. Resource Oriented Programming: Resources are different from objects that are seen in Object Oriented Programming in the sense that you want to make sure that resources are not accidentally lost nor duplicated. Building applications for digital assets with a resource oriented programming language helps enforce asset security.

# 02 - Chapter 2 Quests

<img src="https://as1.ftcdn.net/v2/jpg/03/15/18/50/1000_F_315185021_kql62wZ0zfXTvZ5HAxMYVg7sbYYX6mzg.jpg" alt="cat with good sushi" width="600"/>

## Chapter 2 Day 1

### CH2D1 Quest 1: Deploy a contract to account 0x03 called "JacobTucker"
- Deploy a contract to account 0x03 called "JacobTucker". 
- Inside that contract, declare a constant variable named is, and make it have type String. 
- Initialize it to "the best" when your contract gets deployed.

<img src="https://raw.githubusercontent.com/bz-hashtag-0780/Flow-Zero-to-Jacob/main/quests/screenshots/CH2D1Q1.png" alt="drawing" width="600"/>

### CH2D1 Quest 2: Check that your variable is actually equals "the best".
- Check that your variable is actually equals "the best" by executing a script to read that variable. 
- Include a screenshot of the output.

<img src="https://raw.githubusercontent.com/bz-hashtag-0780/Flow-Zero-to-Jacob/main/quests/screenshots/CH2D1Q2.png" alt="drawing" width="600"/>

## Chapter 2 Day 2

### CH2D2 Quest 1: Explain why we wouldn't call changeGreeting in a script

changeGreeting is a function to modify data which requires running a transaction whereas scripts are used solely for reading data

### CH2D2 Quest 2: What does the AuthAccount mean in the prepare phase of the transaction?

When a transaction gets access to an AuthAccount the transaction will have full access to its data such as storage and public keys.

### CH2D2 Quest 3: What is the difference between the prepare phase and the execute phase in the transaction?

Prepare phase: To access AuthAccount data
Execute phase: To call functions

### CH2D2 Quest 4

- Add two new things inside your contract:
  - A variable named myNumber that has type Int (set it to 0 when the contract is deployed)
  - A function named updateMyNumber that takes in a new number named newNumber as a parameter that has type Int and updates myNumber to be newNumber

<img src="https://raw.githubusercontent.com/bz-hashtag-0780/Flow-Zero-to-Jacob/main/quests/screenshots/CH2D2Q4.1.png" alt="drawing" width="600"/>

- Add a script that reads myNumber from the contract
- Add a transaction that takes in a parameter named myNewNumber and passes it into the updateMyNumber function. Verify that your number changed by running the script again.

<img src="https://raw.githubusercontent.com/bz-hashtag-0780/Flow-Zero-to-Jacob/main/quests/screenshots/CH2D2Q4.2.png" alt="drawing" width="600"/>
Script to read myNumber

<img src="https://raw.githubusercontent.com/bz-hashtag-0780/Flow-Zero-to-Jacob/main/quests/screenshots/CH2D2Q4.3.png" alt="drawing" width="600"/>
Transaction for call updateMyNumber function

<img src="https://raw.githubusercontent.com/bz-hashtag-0780/Flow-Zero-to-Jacob/main/quests/screenshots/CH2D2Q4.4.png" alt="drawing" width="600"/>
Check if function works.

## Chapter 2 Day 3

### CH2D3 Quest 1: In a script, initialize an array (that has length == 3) of your favourite people, represented as `String`s, and `log` it.

<img src="https://raw.githubusercontent.com/bz-hashtag-0780/Flow-Zero-to-Jacob/main/quests/screenshots/CH2D3Q1.png" alt="drawing" width="600" />

### CH2D3 Quest 2: In a script, initialize a dictionary that maps the `String`s Facebook, Instagram, Twitter, YouTube, Reddit, and LinkedIn to a `UInt64` that represents the order in which you use them from most to least. For example, YouTube --> 1, Reddit --> 2, etc. If you've never used one before, map it to 0!

<img src="https://raw.githubusercontent.com/bz-hashtag-0780/Flow-Zero-to-Jacob/main/quests/screenshots/CH2D3Q2.png" alt="drawing" width="600" />

### CH2D3 Quest 3: Explain what the force unwrap operator `!` does, with an example different from the one I showed you (you can just change the type).

It is used to unwrap an optional to its actual type. So `String?` becomes `String`

<img src="https://raw.githubusercontent.com/bz-hashtag-0780/Flow-Zero-to-Jacob/main/quests/screenshots/CH2D3Q3.png" alt="drawing" width="600" />

### CH2D3 Quest 4: Using this picture below, explain...
    - What the error message means
    - Why we're getting this error
    - How to fix it
<img src="https://raw.githubusercontent.com/bz-hashtag-0780/Flow-Zero-to-Jacob/main/chapter2.0/images/wrongcode.png" alt="drawing" width="600" />

The error message says that it expected a String but instead it got a String optional (String or nil)
When dictionaries are accessed, the values returned are optionals. Meaning it might be nil or in the above case a String. The force-unwrap operator `!` must be used to return the actual String type and not just the optional.
It should look like the following

<img src="https://raw.githubusercontent.com/bz-hashtag-0780/Flow-Zero-to-Jacob/main/quests/screenshots/CH2D3Q4.png" alt="drawing" width="600" />

## Chapter 2 Day 4

### CH2D4 Quest 1: Deploy a new contract that has a Struct of your choosing inside of it (must be different than Profile).

<img src="https://raw.githubusercontent.com/bz-hashtag-0780/Flow-Zero-to-Jacob/main/quests/screenshots/CH2D4Q1.png" alt="drawing" width="600" />

### CH2D4 Quest 2: Create a dictionary or array that contains the Struct you defined.

<img src="https://raw.githubusercontent.com/bz-hashtag-0780/Flow-Zero-to-Jacob/main/quests/screenshots/CH2D4Q2.png" alt="drawing" width="600" />

### CH2D4 Quest 3: Create a function to add to that array/dictionary.

<img src="https://raw.githubusercontent.com/bz-hashtag-0780/Flow-Zero-to-Jacob/main/quests/screenshots/CH2D4Q3.png" alt="drawing" width="600" />

### CH2D4 Quest 4: Add a transaction to call that function in step 3.

```cadence
import BasicBeast from 0x02

transaction(dexNumber: UInt32, name: String) {
    
    let currentBeastTemplateID: UInt32

    prepare(acct: AuthAccount) {
        self.currentBeastTemplateID = BasicBeast.nextBeastTemplateID;
      }

    execute {
        BasicBeast.createBeastTemplate(dexNumber: dexNumber, name: name)
    }

    post {
        BasicBeast.getBeastTemplate(beastTemplateID: self.currentBeastTemplateID) != nil:
            "BeastTemplate doesn't exist"
    }
}
```

### CH2D4 Quest 5: Add a script to read the Struct you defined.

```cadence
import BasicBeast from 0x02

pub fun main(beastTemplateID: UInt32): BasicBeast.BeastTemplate {

    let beastTemplate = BasicBeast.getBeastTemplate(beastTemplateID: beastTemplateID)
        ?? panic("BeastTemplate doesn't exist")

    return beastTemplate
}
```

### Running the script

```cadence
17:58:07 get beast template Result:
{"type":"Struct","value":
  {"id":"A.0000000000000002.BasicBeast.BeastTemplate","fields":
    [
        {"name":"beastTemplateID","value":
           {"type":"UInt32","value":"1"}
        },
        {"name":"dexNumber","value":
          {"type":"UInt32","value":"1"}
        },
        {"name":"name","value":
          {"type":"String","value":"Moon"}
         }
      ]
    }
 }

17:58:11 get beast template Result:
{"type":"Struct","value":
  {"id":"A.0000000000000002.BasicBeast.BeastTemplate","fields":
    [
       {"name":"beastTemplateID","value":
          {"type":"UInt32","value":"2"}
        },
       {"name":"dexNumber","value":
          {"type":"UInt32","value":"2"}
        },
       {"name":"name","value":
          {"type":"String","value":"Saber"}
        }
     ]
   }
}
```

# 03 - Chapter 3 Quests

<img src="https://thumbs.dreamstime.com/b/cat-blue-cap-delivers-box-sushi-moped-white-background-scooter-125543441.jpg" alt="driving cat with sushi" width="600"/>

## Chapter 3 Day 1

### CH3D1 Quest 1: List 3 reasons why structs are different from resources
1. Structs can be duplicated
2. Structs can be overwritten
3. Structs can be created whenever needed

### CH3D1 Quest 2: Describe a situation where a resource might be better to use than a struct.
A resource is more secure than a struct and is therefore a better choice to represent NFTs

### CH3D1 Quest 3: What is the keyword to make a new resource?

`create`

### CH3D1 Quest 4: Can a resource be created in a script or transaction (assuming there isn't a public function to create one)?

A resource can't be created in a script nor transaction and only in the smart contract (considering the assumption above).

### CH3D1 Quest 5: What is the type of the resource below?

```cadence
pub resource Jacob {

}
```
The type of the resource is `@Jacob`

### CH3D1 Quest 6: Let's play the "I Spy" game from when we were kids. I Spy 4 things wrong with this code. Please fix them.

```cadence
pub contract Test {

    // Hint: There's nothing wrong here ;)
    pub resource Jacob {
        pub let rocks: Bool
        init() {
            self.rocks = true
        }
    }

    pub fun createJacob(): Jacob { // there is 1 here
        let myJacob = Jacob() // there are 2 here
        return myJacob // there is 1 here
    }
}
```

#### Fixes
```cadence
pub contract Test {

    // Hint: There's nothing wrong here ;)
    pub resource Jacob {
        pub let rocks: Bool
        init() {
            self.rocks = true
        }
    }

    pub fun createJacob(): @Jacob { // 1 fix
        let myJacob <- create Jacob() // 2 fixes
        return <- myJacob // 1 fix
    }
}
```

## Chapter 3 Day 2

### CH3D2 Quest 1: Write your own smart contract that contains two state variables: an array of resources, and a dictionary of resources. Add functions to remove and add to each of them. They must be different from the examples.

#### Resource
```cadence
pub resource NFT {
        pub let id: UInt64

        pub let beastTemplate: BeastTemplate

        init(beastTemplate: BeastTemplate) {
        self.beastTemplate = beastTemplate

        // Increment the global Beast IDs
        BasicBeast.totalSupply = BasicBeast.totalSupply + 1

        // Set unique Beast ID to the newly incremented totalSupply
        self.id = BasicBeast.totalSupply
        }
    }
```

#### Array of NFTs
```cadence
    pub var arrayOfNFTs: @[NFT]

    pub fun addNftToArray(nft: @NFT) {
        self.arrayOfNFTs.append(<- nft)
    }

    pub fun removeNftToArray(index: Int): @NFT {
        return <- self.arrayOfNFTs.remove(at: index)
    }

    init() {
        self.arrayOfNFTs <- []
    } 
```

#### Dictionary of NFTs
```cadence
    pub var dictionaryOfNFTs: @{UInt64: NFT}

    pub fun addNftToDictionary(nft: @NFT) {
        let key = nft.id
        
        self.dictionaryOfNFTs[key] <-! nft
    }

    pub fun removeNftToDictionary(key: UInt64): @NFT {
        let nft <- self.dictionaryOfNFTs.remove(key: key) ?? panic("Could not find the NFT!")
        return <- nft
    }

    init() {
        self.dictionaryOfNFTs <- {}
    }
```

#### Full contract
```cadence
access(all) contract BasicBeast {

    pub var nextBeastTemplateID: UInt32

    pub var totalSupply: UInt64 

    access(self) var beastTemplates: {UInt32: BeastTemplate} 

    pub struct BeastTemplate {
        pub let beastTemplateID: UInt32
        pub let dexNumber: UInt32
        pub let name: String

        init(dexNumber: UInt32, name: String ) {
          pre {
                  name != "": "New BeastTemplate name cannot be blank"
              }

          self.beastTemplateID = BasicBeast.nextBeastTemplateID 
          self.dexNumber = dexNumber
          self.name = name

          // Increment the ID so that it isn't used again
            BasicBeast.nextBeastTemplateID = BasicBeast.nextBeastTemplateID + 1
        }
    }

    pub fun createBeastTemplate(dexNumber: UInt32, name: String): UInt32 {

            // Create the new BeastTemplate
            var newBeastTemplate = BeastTemplate(dexNumber: dexNumber, name: name,)

            let newID = newBeastTemplate.beastTemplateID

            // Store it in the contract storage
            BasicBeast.beastTemplates[newID] = newBeastTemplate

            return newID
        }

    pub fun getBeastTemplate(beastTemplateID: UInt32): BasicBeast.BeastTemplate? {
        return self.beastTemplates[beastTemplateID]
    }

    // NFT non-conforming to the NFT standard
    pub resource NFT {
        pub let id: UInt64

        pub let beastTemplate: BeastTemplate

        init(beastTemplate: BeastTemplate) {
        self.beastTemplate = beastTemplate

        // Increment the global Beast IDs
        BasicBeast.totalSupply = BasicBeast.totalSupply + 1

        // Set unique Beast ID to the newly incremented totalSupply
        self.id = BasicBeast.totalSupply
        }
    }

    // Dictionary of NFTs

    pub var dictionaryOfNFTs: @{UInt64: NFT}

    pub fun addNftToDictionary(nft: @NFT) {
        let key = nft.id
        
        self.dictionaryOfNFTs[key] <-! nft
    }

    pub fun removeNftToDictionary(key: UInt64): @NFT {
        let nft <- self.dictionaryOfNFTs.remove(key: key) ?? panic("Could not find the NFT!")
        return <- nft
    }

    // Array of NFTs

    pub var arrayOfNFTs: @[NFT]
    
    pub fun addNftToArray(nft: @NFT) {
        self.arrayOfNFTs.append(<- nft)
    }

    pub fun removeNftToArray(index: Int): @NFT {
        return <- self.arrayOfNFTs.remove(at: index)
    }
    

    init() {
        self.nextBeastTemplateID = 1
        self.beastTemplates = {}
        self.totalSupply = 0

        self.dictionaryOfNFTs <- {}
        self.arrayOfNFTs <- []
    }

}

```

## Chapter 3 Day 3

### CH3D3 Quest 1: Define your own contract that stores a dictionary of resources. Add a function to get a reference to one of the resources in the dictionary.

```cadence
pub contract BasicBeast {

    pub var totalSupply: UInt64

    pub var dictionaryOfBeasts: @{UInt64: Beast}

    pub resource Beast {
        pub let id: UInt64
        pub let name: String

        init(name: String) {
            self.name = name

            // Increment the global Beast IDs
            BasicBeast.totalSupply = BasicBeast.totalSupply + 1

            // Set unique Beast ID to the newly incremented totalSupply
            self.id = BasicBeast.totalSupply
        }
    }

    pub fun getReference(key: UInt64): &Beast {
        return &self.dictionaryOfBeasts[key] as &Beast
    }

    init() {
        self.totalSupply = 0

        self.dictionaryOfBeasts <- {
            1: <- create Beast(name: "Moon"), 
            2: <- create Beast(name: "Saber")
        }
    }
    
}
```

### CH3D3 Quest 2: Create a script that reads information from that resource using the reference from the function you defined in part 1.

#### Script
```cadence
import BasicBeast from 0x04

pub fun main(): String {
  let ref = BasicBeast.getReference(key: 2)
  return ref.name
}
```
#### Result
```cadence 
22:25:35 read resource Result
{"type":"String","value":"Moon"}

22:25:45 read resource Result
{"type":"String","value":"Saber"}
```

### CH3D3 Quest 3: Explain, in your own words, why references can be useful in Cadence.

We want to use references because moving a resource just to read or update its data is a pain in the ass.

## Chapter 3 Day 4

### CH3D4 Quest 1: Explain, in your own words, the 2 things resource interfaces can be used for (we went over both in today's content)
1. Interfaces are used as requirements. When an interface is implemented by a resource, the resource must conform to the interface's fields and functions.
2. Interfaces are used to expose stuff. Using interfaces makes it possible to expose only some functions to a certain user.

### CH3D4 Quest 2: Define your own contract. Make your own resource interface and a resource that implements the interface. Create 2 functions. In the 1st function, show an example of not restricting the type of the resource and accessing its content. In the 2nd function, show an example of restricting the type of the resource and NOT being able to access its content.

```cadence
pub contract BasicBeast {

    pub var totalSupply: UInt64

    pub resource interface IBeast {
        pub let id: UInt64
        pub let name: String
        pub var nickname: String
    }

    pub resource Beast: IBeast {
        pub let id: UInt64
        pub let name: String
        pub var nickname: String

        init(name: String) {
            self.name = name

            self.nickname = ""

            // Increment the global Beast IDs
            BasicBeast.totalSupply = BasicBeast.totalSupply + 1

            // Set unique Beast ID to the newly incremented totalSupply
            self.id = BasicBeast.totalSupply
        }

        pub fun changeNickname(nickname: String) {
            self.nickname = nickname
        }
    }

    pub fun updateNicknameWithoutInterface() {
        let beast: @Beast <- create Beast(name: "Moon")
        beast.changeNickname(nickname: "New")
        log(beast.nickname) // "New"

        destroy beast
    }

    // Restricted
    pub fun updateNicknameInterface() {
      let beast: @Beast{IBeast} <- create Beast(name: "Moon")
        beast.changeNickname(nickname: "New")
        log(beast.nickname) // "New"

        destroy beast
    }

    init() {
        self.totalSupply = 0
    }
    
}
```

### CH3D4 Quest 3: How would we fix this code? 

```cadence
pub contract Stuff {

    pub struct interface ITest {
      pub var greeting: String
      pub var favouriteFruit: String
    }

    // ERROR:
    // `structure Stuff.Test does not conform 
    // to structure interface Stuff.ITest`
    pub struct Test: ITest {
      pub var greeting: String

      pub fun changeGreeting(newGreeting: String): String {
        self.greeting = newGreeting
        return self.greeting // returns the new greeting
      }

      init() {
        self.greeting = "Hello!"
      }
    }

    pub fun fixThis() {
      let test: Test{ITest} = Test()
      let newGreeting = test.changeGreeting(newGreeting: "Bonjour!") // ERROR HERE: `member of restricted type is not accessible: changeGreeting`
      log(newGreeting)
    }
}
```

#### The fix

```cadence
pub contract Stuff {

    pub struct interface ITest {
      pub var greeting: String
      pub var favouriteFruit: String
      pub fun changeGreeting(newGreeting: String): String // Add this to make the function accessible
    }

    // ERROR FIXED
    pub struct Test: ITest {
      pub var greeting: String
      pub var favouriteFruit: String // Add this to conform to the ITest interface

      pub fun changeGreeting(newGreeting: String): String {
        self.greeting = newGreeting
        return self.greeting // returns the new greeting
      }

      init() {
        self.greeting = "Hello!"
        self.favouriteFruit = "Bacon" // Initialize
      }
    }

    pub fun fixThis() {
      let test: Test{ITest} = Test()
      let newGreeting = test.changeGreeting(newGreeting: "Bonjour!") // ERROR FIXED
      log(newGreeting)
    }
}
```

## Chapter 3 Day 5

### CH3D5 Quest 1: For today's quest, you will be looking at a contract and a script. You will be looking at 4 variables (a, b, c, d) and 3 functions (publicFunc, contractFunc, privateFunc) defined in `SomeContract`. In each AREA (1, 2, 3, and 4), I want you to do the following: for each variable (a, b, c, and d), tell me in which areas they can be read (read scope) and which areas they can be modified (write scope). For each function (publicFunc, contractFunc, and privateFunc), simply tell me where they can be called.

```cadence
access(all) contract SomeContract {
    pub var testStruct: SomeStruct

    pub struct SomeStruct {

        //
        // 4 Variables
        //

        pub(set) var a: String

        pub var b: String

        access(contract) var c: String

        access(self) var d: String

        //
        // 3 Functions
        //

        pub fun publicFunc() {}

        access(contract) fun contractFunc() {}

        access(self) fun privateFunc() {}


        pub fun structFunc() {
            /**************/
            /*** AREA 1 ***/
            /**************/
            
            // a: read and write
            // b: read and write
            // c: read and write
            // d: read and write
            
            // publicFunc() can be called here
            // contractFunc() can be called here
            // privateFunc() can be called here
        }

        init() {
            self.a = "a"
            self.b = "b"
            self.c = "c"
            self.d = "d"
        }
    }

    pub resource SomeResource {
        pub var e: Int

        pub fun resourceFunc() {
            /**************/
            /*** AREA 2 ***/
            /**************/
            
            // a: read and write
            // b: read
            // c: read
            // d: no access
            
            // publicFunc() can be called here
            // contractFunc() can be called here
        }

        init() {
            self.e = 17
        }
    }

    pub fun createSomeResource(): @SomeResource {
        return <- create SomeResource()
    }

    pub fun questsAreFun() {
        /**************/
        /*** AREA 3 ****/
        /**************/
        
        // a: read and write
        // b: read
        // c: read
        // d: no access
        
        // publicFunc() can be called here
        // contractFunc() can be called here
    }

    init() {
        self.testStruct = SomeStruct()
    }
}
```

This is a script that imports the contract above:
```cadence
import SomeContract from 0x01

pub fun main() {
  /**************/
  /*** AREA 4 ***/
  /**************/
  
    // a: read // write in a transaction but not in a script
    // b: read
    // c: no access
    // d: no access
    
    // publicFunc() can be called here
}
```

# 04 - Chapter 4 Quests

<img src="https://thumbs.dreamstime.com/b/cat-funny-hat-hot-dog-holds-paper-cup-coffee-white-background-135301661.jpg" alt="cat with hot dogs" width="600"/>

## Chapter 4 Day 1

### CH4D1 Quest 1: Explain what lives inside of an account. 
Inside an account you can deploy `contract code` and you can deploy multiple smart contracts to the same account. An account also has an `account storage` to store all of its data.

### CH4D1 Quest 2: What is the difference between the `/storage/`, `/public/`, and `/private/` paths?
`/storage/` can only be accessed by the account owner
`/public/` is available to everyone
`/private/` is available to the account owner and other accounts that the account owner has given access to

### CH4D1 Quest 3: What does `.save()` do? What does `.load()` do? What does `.borrow()` do?

`.save()`: To save data to an `account storage` path
`.load()`: To load data from the `account storage`
`.borrow()`: To get a reference to a resource in the `account storage`

### CH4D1 Quest 4: Explain why we couldn't save something to our account storage inside of a script.

Because you need to sign an transaction as the AuthAccount to get access to the `account storage` and save something to it.

### CH4D1 Quest 5: Explain why I couldn't save something to your account.

Because I need to sign a transaction in order to to do so or sign an transaction that gives you the capability to save something to my `account storage`

### CH4D1 Quest 6: Define a contract that returns a resource that has at least 1 field in it. Then, write 2 transactions:

    1) A transaction that first saves the resource to account storage, then loads it out of account storage, logs a field inside the resource, and destroys it.

    2) A transaction that first saves the resource to account storage, then borrows a reference to it, and logs a field inside the resource.
    
#### Some random contract
```cadence
pub contract BasicBeast {

    pub var totalSupply: UInt64

    pub resource interface IBeast {
        pub let id: UInt64
        pub let name: String
        pub var nickname: String
        pub fun changeNickname(nickname: String)
    }

    pub resource Beast: IBeast {
        pub let id: UInt64
        pub let name: String
        pub var nickname: String

        init(name: String) {
            self.name = name

            self.nickname = ""

            // Increment the global Beast IDs
            BasicBeast.totalSupply = BasicBeast.totalSupply + 1

            // Set unique Beast ID to the newly incremented totalSupply
            self.id = BasicBeast.totalSupply
        }

        pub fun changeNickname(nickname: String) {
            self.nickname = nickname
        }
    }

    pub fun updateNicknameWithoutInterface() {
        let beast: @Beast <- create Beast(name: "Moon")
        beast.changeNickname(nickname: "New")
        log(beast.nickname) // "New"

        destroy beast
    }

    // Restricted
    pub fun updateNicknameInterface() {
      let beast: @Beast{IBeast} <- create Beast(name: "Moon")
        beast.changeNickname(nickname: "New")
        log(beast.nickname) // "New"

        destroy beast
    }

    pub fun createBeast(name: String): @Beast {
    return <- create Beast(name: name)
  }

    init() {
        self.totalSupply = 0
    }
    
}
```
#### Transaction 1 load()
```cadence
import BasicBeast from 0x05

transaction(name: String) {
  prepare(signer: AuthAccount) {
    // Save the resource to account storage
    signer.save(<- BasicBeast.createBeast(name: name), to: /storage/MyBeastStorage)

    // Load the resource from the account storage
    let beast <- signer.load<@BasicBeast.Beast>(from: /storage/MyBeastStorage)
                  ?? panic("A `@BasicBeast.Beast` resource does not exist")

    // Log a field
    log(beast.name)

    // Destroy the bastard
    destroy beast
  }

  execute {

  }
}
```

#### Transaction 2 borrow()
```cadence
import BasicBeast from 0x05

transaction(name: String) {
  prepare(signer: AuthAccount) {
    // Save the resource to account storage
    signer.save(<- BasicBeast.createBeast(name: name), to: /storage/MyBeastStorage)

    // Load the resource from the account storage
    let beast = signer.borrow<&BasicBeast.Beast>(from: /storage/MyBeastStorage)
                  ?? panic("A `@BasicBeast.Beast` resource does not exist")

    // Log a field
    log(beast.name)
  }

  execute {

  }
}
```
## Chapter 4 Day 2

### CH4D2 Quest 1: What does `.link()` do?

It links a capability for some data to either the /public/ or /private/ path so others can access the data.

### CH4D2 Quest 2: In your own words (no code), explain how we can use resource interfaces to only expose certain things to the `/public/` path.

Resource interfaces can expose certain things to the `/public/` path by only exposing certain functions in the interface.

### CH4D2 Quest 3: Deploy a contract that contains a resource that implements a resource interface. Then, do the following:

    1) In a transaction, save the resource to storage and link it to the public with the restrictive interface. 

    2) Run a script that tries to access a non-exposed field in the resource interface, and see the error pop up.

    3) Run the script and access something you CAN read from. Return it from the script.

#### Contract with a resource that implements an interface
```cadence
pub contract BasicBeast {

    pub var totalSupply: UInt64

    pub resource interface IBeast {
        pub let id: UInt64
        // Restrict from accessing name
        // pub let name: String
        pub var nickname: String
        pub fun changeNickname(nickname: String)
    }

    pub resource Beast: IBeast {
        pub let id: UInt64
        pub let name: String
        pub var nickname: String

        init(name: String) {
            self.name = name

            self.nickname = ""

            // Increment the global Beast IDs
            BasicBeast.totalSupply = BasicBeast.totalSupply + 1

            // Set unique Beast ID to the newly incremented totalSupply
            self.id = BasicBeast.totalSupply
        }

        pub fun changeNickname(nickname: String) {
            self.nickname = nickname
        }
    }

    pub fun updateNicknameWithoutInterface() {
        let beast: @Beast <- create Beast(name: "Moon")
        beast.changeNickname(nickname: "New")
        log(beast.nickname) // "New"

        destroy beast
    }

    // Restricted
    pub fun updateNicknameInterface() {
      let beast: @Beast{IBeast} <- create Beast(name: "Moon")
        beast.changeNickname(nickname: "New")
        log(beast.nickname) // "New"

        destroy beast
    }

    pub fun createBeast(name: String): @Beast {
    return <- create Beast(name: name)
  }

    init() {
        self.totalSupply = 0
    }
    
}
```
#### Transaction save and link resource with a restrictive interface
```cadence
import BasicBeast from 0x05

transaction(name: String) {

  prepare(signer: AuthAccount) {

    // Save the resource to account storage
    signer.save(<- BasicBeast.createBeast(name: name), to: /storage/MyBeastStorage)

    // link the resource from the account storage
    signer.link<&BasicBeast.Beast{BasicBeast.IBeast}>(/public/MyBeastStorage, target: /storage/MyBeastStorage)
                  ?? panic("A `@BasicBeast.Beast` resource does not exist")
  }

  execute {}
}
```
#### Script with error that can't access restricted field `name`
```cadence
import BasicBeast from 0x05

pub fun main(address: Address): String {

  let publicCapability: Capability<&BasicBeast.Beast{BasicBeast.IBeast}> =
    getAccount(address).getCapability<&BasicBeast.Beast{BasicBeast.IBeast}>(/public/MyBeastStorage)

  let beast: &BasicBeast.Beast{BasicBeast.IBeast} = publicCapability.borrow() ?? panic("The capability doesn't exist or you did not specify the right type when you got the capability.")

  return beast.name // ERROR: member of restricted type is not accessible: name
}
```
#### Script that can access a non-restricted field `id`
```cadence
import BasicBeast from 0x05

pub fun main(address: Address): UInt64 {

  let publicCapability: Capability<&BasicBeast.Beast{BasicBeast.IBeast}> =
    getAccount(address).getCapability<&BasicBeast.Beast{BasicBeast.IBeast}>(/public/MyBeastStorage)

  let beast: &BasicBeast.Beast{BasicBeast.IBeast} = publicCapability.borrow() ?? panic("The capability doesn't exist or you did not specify the right type when you got the capability.")

  return beast.id
}
```
## Chapter 4 Day 3

### CH4D3 Quest 1: What do you have to do if you have resources "nested" inside of another resource? ("Nested resources")

When you have nested resources you must define a `destroy()` function so the nested resource either gets destroyed or moved when the parent resource is destroyed.

### CH4D3 Quest 2: Brainstorm some extra things we may want to add to this contract. Think about what might be problematic with this contract and how we could fix it.

#### Idea #1: Do we really want everyone to be able to mint an NFT?.
If we don't want everyone to be able to mint. We could restrict the function using an interface or creating a resource where only accounts with the resource is able to call the mint function.

#### Idea #2: If we want to read information about our NFTs inside our Collection, right now we have to take it out of the Collection to do so. Is this good?
No, a better way would be to use references

## Chapter 4 Day 4

### CH4D4 Quest 1: Can you brainstorm any ways to distribute Minters to other people WITHOUT having to have 2 signers, or in other words, 2 AuthAccounts?

By creating a capabilitity `link()` of the 'Admin' and let the other account `borrow()` the capability to mint

# 05 - Chapter 5 Quests

<img src="https://as2.ftcdn.net/v2/jpg/02/02/03/25/1000_F_202032588_eFzZSVAQvwLCCGcp3bR7CThPbdEPCFVg.jpg" alt="cat with a lot of sushi" width="600"/>

## Chapter 5 Day 1

### CH5D1 Quest 1: Describe what an event is, and why it might be useful to a client.

Events are emitted to the blockchain when executing functions. It's used so others know what has happened. This way we can be updated about a certain smart contract without having to manually check once a day, every hour or every minute.

### CH5D1 Quest 2: Deploy a contract with an event in it, and emit the event somewhere else in the contract indicating that it happened.

```cadence
pub contract BasicBeast {

    pub event BeastMinted(id: UInt64)

    pub var totalSupply: UInt64

    pub resource interface IBeast {
        pub let id: UInt64
        // Restrict from accessing name
        // pub let name: String
        pub var nickname: String
        pub fun changeNickname(nickname: String)
    }

    pub resource Beast: IBeast {
        pub let id: UInt64
        pub let name: String
        pub var nickname: String

        init(name: String) {
            self.name = name

            self.nickname = ""

            // Increment the global Beast IDs
            BasicBeast.totalSupply = BasicBeast.totalSupply + 1

            // Set unique Beast ID to the newly incremented totalSupply
            self.id = BasicBeast.totalSupply

            emit BeastMinted(id: self.id)
        }

        pub fun changeNickname(nickname: String) {
            self.nickname = nickname
        }
    }

    pub fun updateNicknameWithoutInterface() {
        let beast: @Beast <- create Beast(name: "Moon")
        beast.changeNickname(nickname: "New")
        log(beast.nickname) // "New"

        destroy beast
    }

    // Restricted
    pub fun updateNicknameInterface() {
      let beast: @Beast{IBeast} <- create Beast(name: "Moon")
        beast.changeNickname(nickname: "New")
        log(beast.nickname) // "New"

        destroy beast
    }

    pub fun createBeast(name: String): @Beast {
    return <- create Beast(name: name)
  }

    init() {
        self.totalSupply = 0
    }
    
}
```

### CH5D1 Quest 3: Using the contract in step 2), add some pre conditions and post conditions to your contract to get used to writing them out.

```cadence
pub contract BasicBeast {

    pub event BeastMinted(id: UInt64)

    pub var totalSupply: UInt64

    pub resource interface IBeast {
        pub let id: UInt64
        // Restrict from accessing name
        // pub let name: String
        pub var nickname: String
        pub fun changeNickname(nickname: String)
    }

    pub resource Beast: IBeast {
        pub let id: UInt64
        pub let name: String
        pub var nickname: String

        init(name: String) {
          pre {
                  name != "": "New BeastTemplate name cannot be blank"
              }
            self.name = name

            self.nickname = ""

            // Increment the global Beast IDs
            BasicBeast.totalSupply = BasicBeast.totalSupply + 1

            // Set unique Beast ID to the newly incremented totalSupply
            self.id = BasicBeast.totalSupply

            emit BeastMinted(id: self.id)
        }

        pub fun changeNickname(nickname: String) {
            post {
                self.nickname != "": "The nickname is not blank."
            }
            self.nickname = nickname
        }
    }

    pub fun updateNicknameWithoutInterface() {
        let beast: @Beast <- create Beast(name: "Moon")
        beast.changeNickname(nickname: "New")
        log(beast.nickname) // "New"

        destroy beast
    }

    // Restricted
    pub fun updateNicknameInterface() {
      let beast: @Beast{IBeast} <- create Beast(name: "Moon")
        beast.changeNickname(nickname: "New")
        log(beast.nickname) // "New"

        destroy beast
    }

    pub fun createBeast(name: String): @Beast {
    return <- create Beast(name: name)
  }

    init() {
        self.totalSupply = 0
    }
    
}
```

### CH5D1 Quest 4: For each of the functions below (numberOne, numberTwo, numberThree), follow the instructions.

```cadence
pub contract Test {

  // TODO
  // Tell me whether or not this function will log the name.
  // name: 'Jacob'
  // It will log the name 'Jacob' as long as the input is 'Jacob'
  pub fun numberOne(name: String) {
    pre {
      name.length == 5: "This name is not cool enough."
    }
    log(name)
  }

  // TODO
  // Tell me whether or not this function will return a value.
  // name: 'Jacob'
  // It will not return the name 'Jacob' but will return any input name that is valid and add ' Tucker' in the end of it
  pub fun numberTwo(name: String): String {
    pre {
      name.length >= 0: "You must input a valid name."
    }
    post {
      result == "Jacob Tucker"
    }
    return name.concat(" Tucker")
  }

  pub resource TestResource {
    pub var number: Int

    // TODO
    // Tell me whether or not this function will log the updated number.
    // Also, tell me the value of `self.number` after it's run.
    // self.number will be 1 but the post-condition would make the function fail.
    pub fun numberThree(): Int {
      post {
        before(self.number) == result + 1
      }
      self.number = self.number + 1
      return self.number
    }

    init() {
      self.number = 0
    }

  }

}
```

## Chapter 5 Day 2

### CH5D2 Quest 1: Explain why standards can be benefitial to the Flow ecosystem.

Having standards makes it possible for many different applications to work with many types of digital assets as they all follow the same structure. It allows for scalability and helps make the ecosystem grow much faster.

### CH5D2 Quest 2: What is YOUR favourite food?

<img src="https://c.tenor.com/rd6D2wMN7psAAAAd/burger-food.gif" alt="drawing" width="600"/>

### CH5D2 Quest 3:. Please fix this code (Hint: There are two things wrong):

The contract interface:
```cadence
pub contract interface ITest {
  pub var number: Int
  
  pub fun updateNumber(newNumber: Int) {
    pre {
      newNumber >= 0: "We don't like negative numbers for some reason. We're mean."
    }
    post {
      self.number == newNumber: "Didn't update the number to be the new number."
    }
  }

  pub resource interface IStuff {
    pub var favouriteActivity: String
  }

  pub resource Stuff: IStuff { //Must implement the interface
    pub var favouriteActivity: String
  }
}
```

The implementing contract:
```cadence
import ITest from 0xWherever

pub contract Test: ITest { //Make sure the contract actually implements the ITest
  pub var number: Int
  
  pub fun updateNumber(newNumber: Int) {
    self.number = newNumber
  }

  pub resource Stuff: ITest.IStuff {
    pub var favouriteActivity: String

    init() {
      self.favouriteActivity = "Playing League of Legends."
    }
  }

  init() {
    self.number = 0
  }
}
```

## Chapter 5 Day 3

### CH5D3 Quest 1: What does "force casting" with `as!` do? Why is it useful in our Collection?

It helps us make sure only a specific type of resource can be stored into our collection.

### CH5D3 Quest 2: What does `auth` do? When do we use it?

`auth` reference is what we must use in order to get a downcasted reference.

### CH5D3 Quest 3: This last quest will be your most difficult yet. Take this contract:

```cadence
import NonFungibleToken from 0x02
pub contract CryptoPoops: NonFungibleToken {
  pub var totalSupply: UInt64

  pub event ContractInitialized()
  pub event Withdraw(id: UInt64, from: Address?)
  pub event Deposit(id: UInt64, to: Address?)

  pub resource NFT: NonFungibleToken.INFT {
    pub let id: UInt64

    pub let name: String
    pub let favouriteFood: String
    pub let luckyNumber: Int

    init(_name: String, _favouriteFood: String, _luckyNumber: Int) {
      self.id = self.uuid

      self.name = _name
      self.favouriteFood = _favouriteFood
      self.luckyNumber = _luckyNumber
    }
  }

  pub resource Collection: NonFungibleToken.Provider, NonFungibleToken.Receiver, NonFungibleToken.CollectionPublic {
    pub var ownedNFTs: @{UInt64: NonFungibleToken.NFT}

    pub fun withdraw(withdrawID: UInt64): @NonFungibleToken.NFT {
      let nft <- self.ownedNFTs.remove(key: withdrawID) 
            ?? panic("This NFT does not exist in this Collection.")
      emit Withdraw(id: nft.id, from: self.owner?.address)
      return <- nft
    }

    pub fun deposit(token: @NonFungibleToken.NFT) {
      let nft <- token as! @NFT
      emit Deposit(id: nft.id, to: self.owner?.address)
      self.ownedNFTs[nft.id] <-! nft
    }

    pub fun getIDs(): [UInt64] {
      return self.ownedNFTs.keys
    }

    pub fun borrowNFT(id: UInt64): &NonFungibleToken.NFT {
      return &self.ownedNFTs[id] as &NonFungibleToken.NFT
    }

    init() {
      self.ownedNFTs <- {}
    }

    destroy() {
      destroy self.ownedNFTs
    }
  }

  pub fun createEmptyCollection(): @NonFungibleToken.Collection {
    return <- create Collection()
  }

  pub resource Minter {

    pub fun createNFT(name: String, favouriteFood: String, luckyNumber: Int): @NFT {
      return <- create NFT(_name: name, _favouriteFood: favouriteFood, _luckyNumber: luckyNumber)
    }

    pub fun createMinter(): @Minter {
      return <- create Minter()
    }

  }

  init() {
    self.totalSupply = 0
    emit ContractInitialized()
    self.account.save(<- create Minter(), to: /storage/Minter)
  }
}
```

and add a function called `borrowAuthNFT` just like we did in the section called "The Problem" above. Then, find a way to make it publically accessible to other people so they can read our NFT's metadata. Then, run a script to display the NFTs metadata for a certain `id`.

You will have to write all the transactions to set up the accounts, mint the NFTs, and then the scripts to read the NFT's metadata.


#### Contract
```cadence
import NonFungibleToken from 0x01

pub contract CryptoPoops: NonFungibleToken {
  pub var totalSupply: UInt64

  pub event ContractInitialized()
  pub event Withdraw(id: UInt64, from: Address?)
  pub event Deposit(id: UInt64, to: Address?)

  pub resource NFT: NonFungibleToken.INFT {
    pub let id: UInt64

    pub let name: String
    pub let favouriteFood: String
    pub let luckyNumber: Int

    init(_name: String, _favouriteFood: String, _luckyNumber: Int) {
      self.id = self.uuid

      self.name = _name
      self.favouriteFood = _favouriteFood
      self.luckyNumber = _luckyNumber
    }
  }

  pub resource interface CollectionPublic {
    pub fun deposit(token: @NonFungibleToken.NFT)
    pub fun getIDs(): [UInt64]
    pub fun borrowAuthNFT(id: UInt64): &NFT
  }

  pub resource Collection: NonFungibleToken.Provider, NonFungibleToken.Receiver, NonFungibleToken.CollectionPublic, CollectionPublic {
    pub var ownedNFTs: @{UInt64: NonFungibleToken.NFT}

    pub fun withdraw(withdrawID: UInt64): @NonFungibleToken.NFT {
      let nft <- self.ownedNFTs.remove(key: withdrawID) 
            ?? panic("This NFT does not exist in this Collection.")
      emit Withdraw(id: nft.id, from: self.owner?.address)
      return <- nft
    }

    pub fun deposit(token: @NonFungibleToken.NFT) {
      let nft <- token as! @NFT
      emit Deposit(id: nft.id, to: self.owner?.address)
      self.ownedNFTs[nft.id] <-! nft
    }

    pub fun getIDs(): [UInt64] {
      return self.ownedNFTs.keys
    }

    pub fun borrowNFT(id: UInt64): &NonFungibleToken.NFT {
      return &self.ownedNFTs[id] as &NonFungibleToken.NFT
    }

    pub fun borrowAuthNFT(id: UInt64): &NFT {
      let ref = &self.ownedNFTs[id] as auth &NonFungibleToken.NFT
      return ref as! &NFT
    }

    init() {
      self.ownedNFTs <- {}
    }

    destroy() {
      destroy self.ownedNFTs
    }
  }

  pub fun createEmptyCollection(): @NonFungibleToken.Collection {
    return <- create Collection()
  }

  pub resource Minter {

    pub fun createNFT(name: String, favouriteFood: String, luckyNumber: Int): @NFT {
      return <- create NFT(_name: name, _favouriteFood: favouriteFood, _luckyNumber: luckyNumber)
    }

    pub fun createMinter(): @Minter {
      return <- create Minter()
    }

  }

  init() {
    self.totalSupply = 0
    emit ContractInitialized()
    self.account.save(<- create Minter(), to: /storage/Minter)
  }
}
```


#### Transaction: Setup Collection
```cadence
import NonFungibleToken from 0x01

pub contract CryptoPoops: NonFungibleToken {
  pub var totalSupply: UInt64

  pub event ContractInitialized()
  pub event Withdraw(id: UInt64, from: Address?)
  pub event Deposit(id: UInt64, to: Address?)

  pub resource NFT: NonFungibleToken.INFT {
    pub let id: UInt64

    pub let name: String
    pub let favouriteFood: String
    pub let luckyNumber: Int

    init(_name: String, _favouriteFood: String, _luckyNumber: Int) {
      self.id = self.uuid

      self.name = _name
      self.favouriteFood = _favouriteFood
      self.luckyNumber = _luckyNumber
    }
  }

  pub resource interface CollectionPublic {
    pub fun deposit(token: @NonFungibleToken.NFT)
    pub fun getIDs(): [UInt64]
    pub fun borrowAuthNFT(id: UInt64): &NFT
  }

  pub resource Collection: NonFungibleToken.Provider, NonFungibleToken.Receiver, NonFungibleToken.CollectionPublic, CollectionPublic {
    pub var ownedNFTs: @{UInt64: NonFungibleToken.NFT}

    pub fun withdraw(withdrawID: UInt64): @NonFungibleToken.NFT {
      let nft <- self.ownedNFTs.remove(key: withdrawID) 
            ?? panic("This NFT does not exist in this Collection.")
      emit Withdraw(id: nft.id, from: self.owner?.address)
      return <- nft
    }

    pub fun deposit(token: @NonFungibleToken.NFT) {
      let nft <- token as! @NFT
      emit Deposit(id: nft.id, to: self.owner?.address)
      self.ownedNFTs[nft.id] <-! nft
    }

    pub fun getIDs(): [UInt64] {
      return self.ownedNFTs.keys
    }

    pub fun borrowNFT(id: UInt64): &NonFungibleToken.NFT {
      return &self.ownedNFTs[id] as &NonFungibleToken.NFT
    }

    pub fun borrowAuthNFT(id: UInt64): &NFT {
      let ref = &self.ownedNFTs[id] as auth &NonFungibleToken.NFT
      return ref as! &NFT
    }

    init() {
      self.ownedNFTs <- {}
    }

    destroy() {
      destroy self.ownedNFTs
    }
  }

  pub fun createEmptyCollection(): @NonFungibleToken.Collection {
    return <- create Collection()
  }

  pub resource Minter {

    pub fun createNFT(name: String, favouriteFood: String, luckyNumber: Int): @NFT {
      return <- create NFT(_name: name, _favouriteFood: favouriteFood, _luckyNumber: luckyNumber)
    }

    pub fun createMinter(): @Minter {
      return <- create Minter()
    }

  }

  init() {
    self.totalSupply = 0
    emit ContractInitialized()
    self.account.save(<- create Minter(), to: /storage/Minter)
  }
}
```

#### Transaction mint NFT 
```cadence
import CryptoPoops from 0x02

transaction(name: String, favouriteFood: String, luckyNumber: Int) {

  let minterRef: &CryptoPoops.Minter

  let collectionRef: &CryptoPoops.Collection{CryptoPoops.CollectionPublic}

  prepare(signer: AuthAccount) {

    if signer.borrow<&CryptoPoops.Collection>(from: /storage/CryptoPoopsCollection) == nil {
    // Save the resource to account storage
    signer.save(<- CryptoPoops.createEmptyCollection(), to: /storage/MyCryptoPoopsCollection)

    // link the resource from the account storage
    signer.link<&CryptoPoops.Collection{CryptoPoops.CollectionPublic}>(/public/MyCryptoPoopsCollection, target: /storage/MyCryptoPoopsCollection)
                  ?? panic("A `@CryptoPoops.Collection` resource does not exist")
    }

    // Get minter reference
    self.minterRef = signer.borrow<&CryptoPoops.Minter>(from: /storage/Minter)
                  ?? panic("Cannot borrow minter reference")

    // Get collection reference
    self.collectionRef = getAccount(signer.address).getCapability<&CryptoPoops.Collection{CryptoPoops.CollectionPublic}>(/public/MyCryptoPoopsCollection)
                        .borrow() ?? panic("Cannot borrow collection reference ")

    
  }

  execute {
    self.collectionRef.deposit(token: <- self.minterRef.createNFT(name: name, favouriteFood: favouriteFood, luckyNumber: luckyNumber))
  }
}
```

#### Script to read poop
```cadence
import CryptoPoops from 0x02

pub fun main(address: Address, id: UInt64) {

  let collectionRef = getAccount(address).getCapability<&CryptoPoops.Collection{CryptoPoops.CollectionPublic}>(/public/MyCryptoPoopsCollection)
                        .borrow() ?? panic("Cannot borrow collection reference ")

  let poopRef = collectionRef.borrowAuthNFT(id: id)
  
  log(poopRef.name)

}
```


