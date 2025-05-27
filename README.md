# MoL-memory-over-lifetimes
Solving catastrophic forgetting using modular memory architecture for AGI
  
Built for AGI. Inspired by the human brain.
                                                                                                                            
## 🚨 Problem

Deep learning models **forget everything** when trained on new tasks.  
This is called **catastrophic forgetting**, and it's one of the biggest blockers in AGI.

If I train a model on cooking, then on chess — it forgets how to cook.


## 💡 My Solution: MoL (Memory over Lifetimes)

I built a new architecture that learns tasks **without forgetting**:

-  **Shared Core**: Like the brain’s general intelligence – reused across all tasks  
-  **Room Adapters**: Each task gets its own small room (adapter layer)  
-  **Memory Compression**: I prune each room to reduce memory usage  
-  **Lifelong Growth**: New rooms can be added without touching old ones  
-  **Automatic Selector**: Detects the task from user input and routes to the right room

> One brain. Many rooms. No forgetting.


## 🔬 Key Experiments

| Test | What I Did | Result |
|------|------------|--------|
| MoL vs EWC vs LwF | Trained tasks one-by-one | MoL retains old task accuracy, others forget |
| Pruning Adapters | Pruned 40% of each room | Saves memory, keeps performance |
| Continual Task Stream | Trained tasks in order | No retraining needed. No forgetting. |
| t-SNE Visualization | Plotted embeddings | Rooms stay separate in shared memory |

Visual proof in `/experiments`


## Repo Structure

```bash
MoL-AGI-memory/
├── README.md              ← You're here
├── MoL_colab.ipynb        ← Main code + demo
├── paper/
│   └── MoL_paper.pdf      ← Research-style paper
├── experiments/
│   ├── tSNE_plot.png
│   ├── accuracy_table.png
│   └── pruning_stats.png
├── website/
│   └── index.md           ← Portfolio website content
