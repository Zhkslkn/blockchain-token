# First Assignment Documentation

In this readme file, described a smart contract solidity code. Actually was created token and it's methods.

## Usage

### Initial amount of tokens, File Assignment.sol

<p align="center">
  <img src = "https://github.com/Zhkslkn/blockchain-token/blob/main/assets/init_tokens.png" width=600>
</p>

### ⏲️ Function getLatestTransactionTimestamp, File Assignment.sol

**Task: Create a function to return the block timestamp of the latest transaction in a human-readable format.**

```solidity
  function getLatestTransactionTimestamp() external returns (uint256) {
      uint256 currentTime = block.timestamp;
      uint256 currentHour = (currentTime / 3600) % 24; // Hour
      uint256 currentMinute = (currentTime / 60) % 60; // Minute
      uint256 currentSecond = currentTime % 60; // Second
      emit Timestamp(currentHour, currentMinute, currentSecond);
      return currentTime;
  }
```

**In log we can see human-readable format time (hours : minute : seconds)**

<p align="center">
  <img src = "https://github.com/Zhkslkn/blockchain-token/blob/main/assets/time_result.png" width=600>
</p>

### Function getAddressTransactionSender, File Assignment.sol

**Task: Implement a function to retrieve the address of the transaction sender.**

```solidity
  function getAddressTransactionSender() external returns (address) {
      emit Sender(msg.sender);
      return msg.sender;
  }
```

**In log we can see a sender address value in key "addr"**

<p align="center">
  <img src = "https://github.com/Zhkslkn/blockchain-token/blob/main/assets/sender_result.png" width=600>
</p>

### Function getTransactionReceiver, File Assignment.sol

**Task: Develop a function to retrieve the address of the transaction receiver.**

```solidity
  function getTransactionReceiver() external returns (address) {
      emit Receiver(address(this));
      return address(this);
  }
```

**In log we can see a receiver address value in key "addr"**

<p align="center">
  <img src = "https://github.com/Zhkslkn/blockchain-token/blob/main/assets/receiver_result.png" width=600>
</p>
