.. _cn_api_tensor_random_randperm:

randperm
-------------------------------

.. py:function:: paddle.randperm(n, dtype="int64", name=None)

返回一个数值在0到n-1、随机排列的1-D Tensor，数据类型为 ``dtype``。

参数
::::::::::::
  - **n** (int) - 随机序列的上限（不包括在序列中），应该大于0。 
  - **dtype** (str|np.dtype，可选) - 输出 Tensor 的数据类型，支持 int32、int64、float32、float64。默认值为 int64。
  - **name** (str，可选) - 操作的名称(可选，默认值为None）。更多信息请参见 :ref:`api_guide_Name`。

返回
::::::::::
  Tensor：一个数值在0到n-1、随机排列的1-D Tensor，数据类型为 ``dtype`` 。

代码示例
::::::::::

.. code-block:: python

    import paddle

    out1 = paddle.randperm(5)
    # [4, 1, 2, 3, 0]  # random

    out2 = paddle.randperm(7, 'int32')
    # [1, 6, 2, 0, 4, 3, 5]  # random
