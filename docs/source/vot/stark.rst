Stark
=====

* `link to paper <https://openaccess.thecvf.com/content/ICCV2021/papers/Yan_Learning_Spatio-Temporal_Transformer_for_Visual_Tracking_ICCV_2021_paper.pdf>`_

* `code in github <https://github.com/researchmm/Stark>`_

Questions
---------

* [N] How does it use a transformer?
* [N] What is the model architecture?
* :ref:`[A] <python312>` Can we upgrade it to python 3.12?


.. _python312:

Run in python 3.12
------------------

Yes, I ran it.

In file ``lib/train/data``:

.. code-block:: python

    # Change this:
    from torch._six import string_classes, int_classes

    # To this:
    string_classes = str
    int_classes = int


In file ``lib/models/stark``:

.. code-block:: python

    # Change this:
    from torchvision.models.utils import load_state_dict_from_url

    # To this:
    from torch.hub import load_state_dict_from_url


pip freeze:

.. code-block:: text

    absl-py==2.1.0
    attributee==0.1.9
    attrs==23.2.0
    bidict==0.23.1
    cachetools==5.3.3
    certifi==2024.6.2
    cffi==1.16.0
    charset-normalizer==3.3.2
    colorama==0.4.6
    coloredlogs==15.0.1
    contourpy==1.2.1
    cycler==0.12.1
    Cython==3.0.10
    dominate==2.9.1
    easydict==1.13
    filelock==3.14.0
    flatbuffers==24.3.25
    fonttools==4.53.0
    fsspec==2024.6.0
    grpcio==1.64.1
    huggingface-hub==0.23.2
    humanfriendly==10.0
    idna==3.7
    Jinja2==3.1.4
    jpeg4py==0.1.4
    jsonpatch==1.33
    jsonpointer==2.4
    jsonschema==4.22.0
    jsonschema-specifications==2023.12.1
    kiwisolver==1.4.5
    lazy-object-proxy==1.10.0
    llvmlite==0.42.0
    lmdb==1.4.1
    Markdown==3.6
    MarkupSafe==2.1.5
    matplotlib==3.9.0
    mpmath==1.3.0
    networkx==3.3
    numba==0.59.1
    numpy==1.26.4
    nvidia-cublas-cu12==12.1.3.1
    nvidia-cuda-cupti-cu12==12.1.105
    nvidia-cuda-nvrtc-cu12==12.1.105
    nvidia-cuda-runtime-cu12==12.1.105
    nvidia-cudnn-cu12==8.9.2.26
    nvidia-cufft-cu12==11.0.2.54
    nvidia-curand-cu12==10.3.2.106
    nvidia-cusolver-cu12==11.4.5.107
    nvidia-cusparse-cu12==12.1.0.106
    nvidia-nccl-cu12==2.20.5
    nvidia-nvjitlink-cu12==12.5.40
    nvidia-nvtx-cu12==12.1.105
    onnx==1.16.1
    onnxruntime-gpu==1.18.0
    opencv-python==4.10.0.82
    ordered-set==4.1.0
    packaging==24.0
    pandas==2.2.2
    phx-class-registry==4.1.0
    pillow==10.3.0
    protobuf==4.25.3
    pycocotools==2.0.7
    pycparser==2.22
    PyLaTeX==1.4.2
    pyparsing==3.1.2
    python-dateutil==2.9.0.post0
    pytz==2024.1
    PyYAML==6.0.1
    referencing==0.35.1
    requests==2.32.3
    rpds-py==0.18.1
    safetensors==0.4.3
    scipy==1.13.1
    setuptools==69.5.1
    six==1.16.0
    sympy==1.12.1
    tb-nightly==2.17.0a20240604
    tensorboard-data-server==0.7.2
    tikzplotlib==0.10.1
    timm==1.0.3
    torch==2.3.0
    torchvision==0.18.0
    tornado==6.4
    tqdm==4.66.4
    typing_extensions==4.12.1
    tzdata==2024.1
    urllib3==2.2.1
    visdom==0.2.4
    vot-toolkit @ git+https://github.com/votchallenge/vot-toolkit-python@0abc8e537ca8c94bf898abae0217529daa272e7d
    vot-trax==4.0.2
    webcolors==1.13
    websocket-client==1.8.0
    Werkzeug==3.0.3
    wheel==0.43.0
    yacs==0.1.8
