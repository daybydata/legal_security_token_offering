# legal_security_token_offering
A project to develop smart contracts for regulated security token offerings.

## Problem

Businesses want new options to raise capital, consumers want to invest in the brands they trust, and institutional investors want alternative (uncorrelated) assets to diversify their holdings.

The crypto solutions to these problems are beleaguered by volatility, fraud, and market manipulation.

It's time to build a new financial ecosystem that combines the protections of SEC regulation with the efficiency, security and liquidity of digital assets.

![Regulation_is_inevitable](https://user-images.githubusercontent.com/94941017/168478549-2edbe604-4bf7-4c07-9607-1172dc89dff0.png)

## The new financial ecosystem needs...

* New (legal) tools for capitalizing business: SEC-registered Security Token Offerings (STOs) using ECR 1404
* A regulated, compliance-first exchange for digital assets
* A pipeline of credible businesses with large audiences and “tribal” power to drive exchange adoption and velocity
* A market facilitator to prepare companies for the compliance requirements of a public offering
* A marketplace for the Insumer* to purchase public shares

*Investor + consumer = Insumer

## ECR 1404

Well-designed smart contracts can help ensure compliance with U.S. securities law automatically, preventing unqualified trades while ensuring transparency and accuracy with every transation.

"ERC-1404 is a simple restricted token standard on Ethereum. The recent development of the ERC-1404 standard has a couple key features differentiating it from other standards; most notably, it holds similar properties to regulated securities. This feature gives the ERC-1404 token the properties to become a publicly traded, tokenized asset."

“The new standard was proposed by TokenSoft, a leading blockchain-solutions company. The ERC-1404 consensus gives token issuers more control over circulation as well as visibility of holders. The ability to freeze supply and identify holders of the token differentiates it from the typical ERC-20 standard often used for altcoins. The ERC-1404 token was the only standard to be filed in multiple U.S. Securities and Exchange Commission (SEC) hearings, which could eventually result in the ability to transfer equities, debt and derivatives with it.”

https://www.benzinga.com/markets/22/05/27058842/what-is-the-significance-of-the-erc1404

The ERC-1404 standard inherits all of the ERC-20 functionality but adds critical new features with just two additional lines of code. The code behind these protocols can be seen below.

ERC 20
```
contract ERC20 {
  function totalSupply() public view returns (uint256);
  function balanceOf(address who) public view returns (uint256);
  function transfer(address to, uint256 value) public returns (bool);
  function allowance(address owner, address spender) public view returns (uint256);
  function transferFrom(address from, address to, uint256 value) public returns (bool);
  function approve(address spender, uint256 value) public returns (bool);
  event Approval(address indexed owner, address indexed spender, uint256 value);
  event Transfer(address indexed from, address indexed to, uint256 value);
}
```
ERC 1404

```
contract ERC1404 is ERC20 {
  function detectTransferRestriction (address from, address to, uint256 value) public view returns (uint8);
  function messageForTransferRestriction (uint8 restrictionCode) public view returns (string);
}





