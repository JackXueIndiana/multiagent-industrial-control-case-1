# multiagent-industrial-control-case-1
AutoGen offers conversable agents powered by LLM, tool, or human, which can be used to perform tasks collectively via automated chat. This framework allows tool use and human participation through multi-agent conversation. Please find documentation about this feature [here](https://microsoft.github.io/autogen/docs/Use-Cases/agent_chat).

The use case is the following: a pH value low alert has been fired by some senser and notified a Chatbot (AssistantAgent) which in turn dispatch a UserProxyAgent to get the time series dataset, conduct a dynamic lower band calculation. If the dataset present datapoints with values lower than the lower band. If so, then calculate the estimated time the drop happened. Based on the results, the agent will suggest making a 'Rate Change'.

By fitting our problem into the sample notebooks referenced, we solve this problem in three ways. 
- pHLowFunction uses UserProxyAgent to call a function written in Python for statistic control process calculation.
- phLowGptCoder uses SocietyOfMindAgent to hide the inter-agent communications' complexity as inner monologues.
- phLowGptWorkflow uses ChatGroup and state_transition to define the workflow and transition critiria.
  
## Requirements

AutoGen requires `Python>=3.8`. To run this notebook example, please install `pyautogen`:
```bash
pip install pyautogen
```

## Reference
~~~
https://github.com/microsoft/autogen/blob/main/notebook/agentchat_function_call_currency_calculator.ipynb
https://github.com/microsoft/autogen/blob/main/notebook/agentchat_society_of_mind.ipynb
https://github.com/microsoft/autogen/blob/main/notebook/agentchat_groupchat_stateflow.ipynb
~~~
