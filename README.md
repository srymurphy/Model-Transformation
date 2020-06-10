# Model-Transformation
darknet to caffe model

python darknet2caffe.py tiny-yolo-voc.cfg tiny-yolo-voc.weights tiny-yolo-voc.prototxt tiny-yolo-voc.caffemodel

darknet to TensorFlow
##Optional Flags 
convert_weights:

    --class_names
        Path to the class names file
    --weights_file
        Path to the desired weights file
    --data_format
        NCHW (gpu only) or NHWC
    --tiny
        Use yolov3-tiny
    --spp
        Use yolov3-spp
    --ckpt_file
        Output checkpoint file

convert_weights_pb.py:

    --class_names 1. Path to the class names file
    --weights_file
        Path to the desired weights file
    --data_format
        NCHW (gpu only) or NHWC
    --tiny
        Use yolov3-tiny
    --spp
        Use yolov3-spp
    --output_graph
        Location to write the output .pb graph to
        
YOLOv3 转ckpt文件格式：
python convert_weights.py --class_names coco.names --data_format NHWC --weights_file yolov3.weights

YOLOv3-tiny 转ckpt文件格式：
python convert_weights.py --class_names coco.names --data_format NHWC --weights_file yolov3-tiny.weights --tiny

YOLOv3 转pb文件格式：
python convert_weights_pb.py --class_names coco.names --data_format NHWC --weights_file yolov3.weights

YOLOv3-tiny 转pb文件格式：
python convert_weights_pb.py --class_names coco.names --data_format NHWC --weights_file yolov3-tiny.weights --tiny
