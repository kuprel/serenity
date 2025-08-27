Simulates God's decision tree

```mermaid
flowchart TD
  PRAY["God, I have a problem, I pray to You for help"]:::prayer
  CHANGE1{"Is There Something You Can Change?"}:::gate
  COURAGE["I Grant You COURAGE To Solve Your Problem"]:::answer
  CHANGE2{"Are You Sure?"}:::gate
  SERENITY["I Grant You SERENITY To Accept The Things You Cannot Change"]:::answer
  WISDOM["Seek WISDOM To Know The Difference"]:::answer

  PRAY --> CHANGE1
  CHANGE1 -- Yes --> COURAGE
  CHANGE1 -- No  --> CHANGE2
  CHANGE2 -- Yes --> SERENITY
  CHANGE2 -- No  --> WISDOM
  WISDOM -. "Come back" .-> CHANGE1
```

## Install

```bash
git clone https://github.com/kuprel/serenity
cd serenity
chmod +x helpgod
```

## Usage

```bash
> ./helpgod
Is There Something You Can Change? (yes/no) yes
I Grant You COURAGE To Solve Your Problem
```

```bash
> ./helpgod
Is There Something You Can Change? (yes/no) no
Are You Sure? (yes/no) yes
I Grant You SERENITY To Accept The Things You Cannot Change
```

```bash
> ./helpgod
Is There Something You Can Change? (yes/no) no
Are You Sure? (yes/no) no
Seek WISDOM To Know The Difference Then Come Back
Is There Something You Can Change? (yes/no) yes
I Grant You COURAGE To Solve Your Problem
```
