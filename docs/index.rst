Welcome to DeeR's documentation!
==================================

DeeR (Deep Reinforcement) is a lightweight python library to train an agent how to behave in a given environement so as to maximize a cumulative sum of rewards.
It is based on the original deep Q learning algorithm described in :
Mnih, Volodymyr, et al. "Human-level control through deep reinforcement learning." Nature 518.7540 (2015): 529-533. (see :ref:`what-is-deer`)

Contrary to the original code, this package provides a more general framework where observations are made up of any number of elements : scalars, vectors and frames (instead of one type of frame only in the above mentionned paper). At each time step, an action is taken by the agent and one observation is gathered (along with one reward). The belief state on which the agent is based to build the Q function is made up of any length history of each element provided in the observation.

Another advantage of this framework is that it is build in such a way that you can easily add up a validation phase that allows to stop the training process before overfitting. This possibility is useful when the environment is dependent on scarce data (e.g. limited time series).

The framework is made in such a way that it is easy to 

* build any environment
* modify any part of the learning process
* use your favorite python-based framework to code your own neural network architecture. The provided neural network architectures are based on Theano but you may easily use another one.

It is a work in progress and input is welcome. Please submit any contribution via pull request.

What is new
------------
Version 0.2 (soon)
******************
- Standalone python package (you can simply do ``pip install deer``)
- Integration of new examples environments : :ref:`toy_env_pendulum`, :ref:`PLE` and :ref:`gym`
- First automated tests
- Double Q-learning and prioritized Experience Replay
- Augmented documentation

Future extensions:
******************

* Add planning (e.g. MCTS based when deterministic environment)
* Several agents interacting in the same environment
* ...

The available documentation is limited for now. For details, the user can refer to comments in the code itself and to the different working examples. An API documentation will be made available in the future.

User Guide
------------

.. toctree::
  :maxdepth: 2
  
  user/installation
  user/tutorial
  user/environments
  user/development
    
API reference
-------------

If you are looking for information on a specific function, class or method, this API is for you.

.. toctree::
  :maxdepth: 2
  
  modules/agents
  modules/controllers
  modules/environments
  modules/q-networks
  
  

Indices and tables
------------------

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

.. _GitHub: https://github.com/VinF/General_Deep_Q_RL