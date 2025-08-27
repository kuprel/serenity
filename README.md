Simulates God's decision tree

```mermaid
flowchart TD
  PRAY["God, I have a problem, I pray to You for help"]:::prayer
  CHANGE1{"Is there something you can change?"}:::gate
  COURAGE["I grant you Courage to solve your problem"]:::answer
  CHANGE2{"Are you sure?"}:::gate
  SERENITY["I grant you Serenity to accept the things you cannot change"]:::answer
  WISDOM["Seek Wisdom to know the difference"]:::answer

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
