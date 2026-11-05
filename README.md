# PyTorch Community Meetup Mbarara

Two hands-on workshops for people who know a little Python and are new to PyTorch. Start by training a small model from scratch, then adapt a pretrained model to a new task.

| Start here | Time | What you'll do |
| --- | --- | --- |
| [1. PyTorch fundamentals](notebooks/pytorch_fundamentals_mbarara.ipynb) | 25 min | Use tensors and train a clothing classifier on Fashion-MNIST. |
| [2. Transfer learning with bean leaves](notebooks/pytorch_transfer_learning_beans_mbarara.ipynb) | 25 min | Adapt ResNet18 to classify bean leaf images from [Makerere AI Lab's Beans dataset](https://huggingface.co/datasets/AI-Lab-Makerere/beans). |

[Download the PowerPoint slides for both workshops](slides/pytorch-meetup-mbarara-workshops.pptx).

## Run in a browser

Download the notebook you want from the table, then upload it to [Google Colab](https://colab.research.google.com/). For workshop 2, run `%pip install datasets` in a new cell before running the workshop cells. A CPU is enough for workshop 1. A GPU, if available, speeds up workshop 2.

## Run locally

From the repository folder, create and activate a virtual environment. For example, in Windows PowerShell:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

On macOS or Linux, activate it with `source .venv/bin/activate`. Use the [PyTorch installation selector](https://pytorch.org/get-started/locally/) to install matching versions of `torch` and `torchvision` for your platform. For a CPU-only setup on Windows or Linux:

```sh
python -m pip install torch torchvision --index-url https://download.pytorch.org/whl/cpu
```

Install the notebook dependencies for the workshop you plan to run, then start Jupyter.

```sh
# Workshop 1 only
python -m pip install -r requirements.txt

# Both workshops, including the Beans dataset loader
python -m pip install -r requirements-beans.txt

python -m notebook
```

In Jupyter, open the notebook under `notebooks/` and run its cells from top to bottom. The first run needs internet to fetch the datasets and, for workshop 2, the pretrained weights.

## For meetup facilitators

Run both notebooks once in the environment you'll use at the venue so downloads are cached. Allow extra time for the Beans workshop on CPU, and keep a local copy with outputs if you want to show the results while participants run their own copies. The bean leaf classifier is a classroom demonstration.
