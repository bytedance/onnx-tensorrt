import os

dep_trt = 'cpp3rdlib/tensorrt@//cpp3rdlib/tensorrt:nvinfer,nvinfer_plugin,nvcaffe_parser'
dep_onnx = '//quicksilver/quicksilver/cc_lib/engine/tensorrt/onnx-tensorrt/third_party:onnx'

deps = [dep_trt, dep_onnx]
defs = ['ONNX_NAMESPACE=onnx']

cc_library(
    name='nvonnxparser',
    incs='',
    srcs=[
        'NvOnnxParser.cpp',
        'ModelImporter.cpp',
        'builtin_op_importers.cpp',
        'onnx2trt_utils.cpp',
        'ShapedWeights.cpp',
        'ShapeTensor.cpp',
        'LoopHelpers.cpp',
        'RNNHelpers.cpp',
        'OnnxAttrs.cpp',
    ],
    deps=deps,
    defs=defs,
    extra_cppflags=['-Wno-missing-field-initializers']
)

cc_binary(
    name='onnx2trt',
    srcs=[
        'main.cpp'
    ],
    deps=[':nvonnxparser'],
    defs=defs
)
