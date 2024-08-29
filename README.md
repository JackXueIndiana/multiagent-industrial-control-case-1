# multiagent-industrial-control-case-1
AutoGen offers conversable agents powered by LLM, tool, or human, which can be used to perform tasks collectively via automated chat. This framework allows tool use and human participation through multi-agent conversation. Please find documentation about this feature [here](https://microsoft.github.io/autogen/docs/Use-Cases/agent_chat).

The use case is the following: a pH value low alert has been fired by some senser and notified a Chatbot (AssistantAgent) which in turn dispatch a UserProxyAgent to get the time series dataset, conduct a dynamic lower band calculation. If the dataset present datapoints with values lower than the lower band. If so, then calculate the estimated time the drop happened. Based on the results, the agent will suggest making a 'Rate Change'.
  
## Requirements

AutoGen requires `Python>=3.8`. To run this notebook example, please install `pyautogen`:
```bash
pip install pyautogen
```
