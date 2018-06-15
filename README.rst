Ray Tutorial
============

To run the tutuorial online, click on the binder link below:



Local Setup
-----------

To install the tutorial on your own machine:

1. Make sure you have installed
`Anaconda <https://www.anaconda.com/download>`__. We recommend Python 3.6.

2. Clone the tutorial repository:

.. code-block:: bash

  git clone https://github.com/ray-project/tutorial.git

3. Install the dependencies from ``enviornment.yml`` using ``conda``:

.. code-block:: bash

    conda env create -f enviornment.yml

Exercises
---------

Each file ``exercises/exercise*.ipynb`` is a separate exercise. They can be
opened in a Jupyter notebook by running the following commands.

.. code-block:: bash

  source activate ray-tutorial
  cd tutorial/exercises
  jupyter-notebook

If it asks for a password, just hit enter.

Instructions are written in each file. To do each exercise, first run all of
the cells in the Jupyter notebook. Then modify the ones that need to be modified
in order to prevent any exceptions from being raised. Throughout these
exercises, you may find the `Ray documentation`_ helpful.

**Exercise 1:** Define a remote function, and execute multiple remote functions
in parallel.

**Exercise 2:** Execute remote functions in parallel with some dependencies.

**Exercise 3:** Pass object IDs into tasks to construct dependencies between
tasks.

**Exercise 4:** Call remote functions from within remote functions.

**Exercise 5:** Use ``ray.wait`` to ignore stragglers. See the
`documentation for wait`_.

**Exercise 6:** Use ``ray.wait`` to process tasks in the order that they finish.
See the `documentation for wait`_.

**Exercise 7:** Use actors to share state between tasks. See the documentation
on `using actors`_.

**Exercise 8:** Pass actor handles to tasks so that multiple tasks can invoke
methods on the same actor.

**Exercise 9:** Use ``ray.put`` to avoid serializing and copying the same
object into shared memory multiple times.

**Exercise 10:** Specify that an actor requires some GPUs. For a complete
example that does something similar, you may want to see the `ResNet example`_.

**Exercise 11:** Specify that a remote function requires certain custom
resources. See the documentation on `custom resources`_.

**Exercise 12:** Extract neural network weights from an actor on one process,
and set them in another actor. You may want to read the documentation on
`using Ray with TensorFlow`_.

.. _`Anaconda Python distribution`: https://www.continuum.io/downloads
.. _`Ray documentation`: http://ray.readthedocs.io/en/latest/?badge=latest
.. _`documentation for wait`: http://ray.readthedocs.io/en/latest/api.html#waiting-for-a-subset-of-tasks-to-finish.
.. _`using actors`: http://ray.readthedocs.io/en/latest/actors.html
.. _`using Ray with TensorFlow`: http://ray.readthedocs.io/en/latest/using-ray-with-tensorflow.html
.. _`ResNet example`: http://ray.readthedocs.io/en/latest/example-resnet.html
.. _`custom resources`: http://ray.readthedocs.io/en/latest/resources.html#custom-resources


More In-Depth Examples
----------------------

**Sharded Parameter Server:** This exercise involves implementing a parameter
server as a Ray actor, implementing a simple asynchronous distributed training
algorithm, and sharding the parameter server to improve throughput.

RL Exercises
------------

Each file in ``rl_exercises/rl_exercise*.ipynb`` is a separate Jupyter notebook.
These exercises should be done in order. They can be opened in a Jupyter
notebook by running the following commands.

.. code-block:: bash

  cd tutorial/rl_exercises
  jupyter-notebook
