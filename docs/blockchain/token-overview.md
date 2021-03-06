# ``$`EDI vs. EDI``

$EDI is the **ERC-20 Token** EDI is the message data structure

$EDI dervices and acrues value by businesses using this to pay for
transactions (i.e. EDI B2B usually over AS2 Protocol). We have an
integrated AS2 protocol into our Hyperledger Besu client that enables
the same functionality as legacy AS2. Freight Trust & Clearing
corporation abstracts away the process of companies using the token
utility by invoicing them for transactions (e.g. Net 30) while paying
for their transaction at the current market rate for the token. More
details on the fixed exchange rate mechanism, called "PEM" can be found
in the RFC section on
[@github-freight-chain/rfc](https://github.com/freight-chain/rfc#issues).

## EDI Messages Priced as Ethereum (per kilobyte/gwei)

| Yellow Paper     | Gwei   | EDI Transaction | Cost in gwei |
| ---------------- | ------ | --------------- | ------------ |
| GxdataZero       | 4      | Segments        | unit256      |
| GxdataNonZero    | 6,800  | Interchange     | 1,136        |
| GxminTransaction | 21,000 | File Data       | 77,248       |

**Calculating Max Supply**

We then dervice a rough estimate of EDI messages sent per block by the
following:

**Genesis file** Gas limit: 0xa00000 gas limit per block (decimal):
10485760

We then Calculate the EDI messages sent per block by using the template
validation EDI file for 211 (bill of lading)

EDI message (in bytes): 1,136 EDI Transaction cost: 77,248 $EDI tx’s per
block: 135.7415079

Max Transcactions per year per 1 token: 428,358,824.8

``` 
  151,113,902
+ 428,358,825 Summation: 611,029,679
```

Citations and Sources: [EVM
Opcodes](https://github.com/nsward/evm-opcodes) [Ethereum Yellow
Paper](http://gavwood.com/paper.pdf)

## EDI Message

``` edi
ISA*00*          *00*          *ZZ*1234567        *ZZ*11111          *170508*1141*^*00501*000000101*1*P*:~
GS*HC*XXXXXXX*XXXXX*20170617*1741*101*X*005010X222A1~
ST*837*0021*005010X222A1~
BHT*0019*00*244579*20061015*1023*CH~
NM1*41*2*PREMIER BILLING SERVICE*****46*TGJ23~
PER*IC*JERRY*TE*3055552222*EX*231~
NM1*40*2*KEY INSURANCE COMPANY*****46*66783JJT~
HL*1**20*1~
PRV*BI*PXC*203BF0100Y~
NM1*85*2*BEN KILDARE SERVICE*****XX*9876543210~
N3*234 SEAWAY ST~
N4*MIAMI*FL*33111~
REF*EI*587654321~
NM1*87*2*Kildare Associates~
N3*2345 OCEAN BLVD~
N4*MIAMI*FL*33111~
HL*2*1*22*1~
SBR*P**2222-SJ******CI~
NM1*IL*1*SMITH*JANE****MI*JS00111223333~
DMG*D8*19430501*F~
NM1*PR*2*KEY INSURANCE COMPANY*****PI*999996666~
REF*G2*KA6663~
HL*3*2*23*0~
PAT*19~
NM1*QC*1*SMITH*TED~
N3*236 N MAIN ST~
N4*MIAMI*FL*33413~
DMG*D8*19730501*M~
CLM*26463774*100***11:B:1*Y*A*Y*I~
REF*D9*17312345600006351~
HI*BK:0340*BF:V7389~
LX*1~
SV1*HC:99213*40*UN*1***1~
DTP*472*D8*20061003~
LX*2~
SV1*HC:87070*15*UN*1***1~
DTP*472*D8*20061003~
LX*3~
SV1*HC:99214*35*UN*1***2~
DTP*472*D8*20061010~
LX*4~
SV1*HC:86663*10*UN*1***2~
DTP*472*D8*20061010~
SE*42*0021~
GE*1*101~
IEA*1*000000101~
```

## Parsing Messages

The **Maidenlane** parser performs critical security validity checks
against the raw `EDI` messages in a `ASCII` stream. When dealing with
`UTF-8` encoded form of its input, it `does not` interpret certain
illegal octet sequences as characters. For example, a parser might
prohibit the `NUL` character when encoded as the single-octet sequence
`00`, but erroneously allow the illegal two-octet sequence `C0 80` and
interpret it as a `NUL` character.

### Example Parser Exploit

**Web Server Exploit.**

An example might be a parser which prohibits the octet sequence
`2F 2E 2E 2F ("/../")`, yet permits the illegal octet sequence `2F C0
AE 2E 2F`.
[<sup>source</sup>](https://tools.ietf.org/html/rfc3629#section-6)

## Coding Ruleset

### Type Structure Theorem

**Design choice to enforce security.**

Types increase your agility when doing refactoring. It’s better for the
compiler to catch errors than to have things fail at runtime. Types are
one of the best forms of documentation you can have. The function
signature is a theorem and the function body is the proof.

[see: Definitely Typed GitHub for an
overview](https://github.com/DefinitelyTyped/DefinitelyTyped)

### Null vs. Undefined

  - Null vs. Undefined
    
    **Not Conforming.**
    
    ``` javascript
    let foo = {x:123,y:undefined};
    ```
    
    **Conforming.**
    
    ``` javascript
    let foo:{x:number,y?:number} = {x:123};
    ```

### Variable and Function Names

Use `camelCase` for variable and function names

  - Variable
    
    **Not Conforming.**
    
    ``` javascript
    var FooVar;
    function BarFunc() { }
    ```
    
    **Conforming.**
    
    ``` typescript
    var fooVar;
    function barFunc() { }
    ```

### Class Names

Use `PascalCase` for class names.

  - Class Name
    
    **Not Conforming.**
    
    ``` javascript
    class foo { }
    ```
    
    **Not Conforming.**
    
    ``` typescript
    class Foo { }
    ```

  - Members and Methods
    
    Use `camelCase` of class members and methods This naturally follows
    from variable and function naming convention
    
    **Not Conforming.**
    
    ``` javascript
    class foo { }
    ```
    
    **Conforming.**
    
    ``` typescript
    class Foo { }
    ```
