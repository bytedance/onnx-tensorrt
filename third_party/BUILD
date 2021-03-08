defs = ['ONNX_NAMESPACE=onnx']

cc_library(
    name='onnx',
    export_incs=['onnx'],
    deps=[':onnx_proto'],
    srcs=[
        'onnx/onnx/optimizer/*.cc',
        'onnx/onnx/common/*.cc',
        'onnx/onnx/defs/*.cc'
    ],
    defs=defs
)

proto_library(
    name='onnx_proto',
    srcs=[
        'onnx/onnx/onnx.proto',
        'onnx/onnx/onnx-operators.proto',
    ]
)