# Planning-Machine
A Machine that plans.

In order to launch it from the command line or as a Python subprocess:
```bash
echo "Theodotos-Alexandreus: Plan the sequence of actions, machine." \
  | uvx planning-machine \
    --provider-api-key=sk-proj-... \
    --github-token=ghp_... 
```

Or, with a local pip installation:
```bash
pip install planning-machine
```
Set the environment variables:
```bash
export PROVIDER_API_KEY="sk-proj-..."
export GITHUB_TOKEN="ghp_..."
```
Then:
```bash
planning-machine multilogue.txt
```
Or:
```bash
planning-machine multilogue.txt new_turn.txt
```
Or:
```bash
cat multilogue.txt | planning-machine
```
Or:
```bash
cat multilogue.txt | planning-machine > tmp && mv tmp multilogue.txt
```
Or: 
```bash
(cat multilogue.txt; echo:"Theodotos: What do you think, Planning-Machine?") \
  | planning-machine
```
Or:
```bash
cat multilogue.txt new_turn.txt | planning-machine
```
Or:
```bash
cat multilogue.txt new_turn.txt | planning-machine >  tmp && mv tmp multilogue.txt
```
Or, if you have installed other machines:
```bash
cat multilogue.md | planning-machine \
  | summarizing-machine | judging-machine > summary_judgment.md
```

Or use it in your Python code:
```Python
# Python
import planning_machine
```
