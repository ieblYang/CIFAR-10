# CIFAR-10
data_manager:   
  &emsp;&emsp;convert_cifar10_image  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;CIFAR-10数据集的下载与解析  
  &emsp;&emsp;writer_cifar10         &nbsp;&emsp;&emsp;&emsp;&emsp;&emsp;CIFAR-10数据集的打包（tfrecord）  
  &emsp;&emsp;reader_cifar10         &nbsp;&nbsp;&nbsp; &nbsp; &nbsp;&emsp;&emsp;&emsp;通过TensorFlow对TFRecord打包过的数据进行解析  
  &emsp;&emsp;reader_cifar10-1       &emsp;&emsp;&emsp;&emsp;通过slice_input_producer读取文件列表中的样本  
  &emsp;&emsp;reader_cifar10-2       &emsp;&emsp;&emsp;&emsp;通过string_input_producer从文件中读取数据  
  
cifar10:   
  &emsp;&emsp;readcifar10  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;通过TensorFlow对TFRecord打包过的数据进行解析 
  &emsp;&emsp;train         &nbsp;&emsp;&emsp;&emsp;&emsp;&emsp;训练  
  &emsp;&emsp;test         &nbsp;&nbsp;&nbsp; &nbsp; &nbsp;&emsp;&emsp;&emsp;测试
  &emsp;&emsp;resnet       &emsp;&emsp;&emsp;&emsp;resnet网络
