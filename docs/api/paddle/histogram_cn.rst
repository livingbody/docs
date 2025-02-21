.. _cn_api_tensor_histogram:

histogram
-------------------------------

.. py:function:: paddle.histogram(input, bins=100, min=0, max=0, name=None)

计算输入 Tensor 的直方图。以 min 和 max 为 range 边界，将其均分成 bins 个直条，然后将排序好的数据划分到各个直条(bins)中。如果 min 和 max 都为0，则利用数据中的最大最小值作为边界。

参数
::::::::::::

    - **input** (Tensor) - 输入Tensor。维度为多维，数据类型为int32、int64、float32或float64。
    - **bins** (int，可选) - 直方图 bins(直条)的个数，默认为100。
    - **min** (int，可选) - range的下边界(包含)，默认为0。
    - **max** (int，可选) - range的上边界(包含)，默认为0。
    - **name** (str，可选) - 具体用法请参见  :ref:`api_guide_Name` ，一般无需设置，默认值为 None。

返回
::::::::::::
Tensor，数据为 int64 类型，维度为(nbins,)。

代码示例
::::::::::::

.. code-block:: python

    import paddle

    inputs = paddle.to_tensor([1, 2, 1])
    result = paddle.histogram(inputs, bins=4, min=0, max=3)
    print(result) # [0, 2, 1, 0]


