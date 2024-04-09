
### train部分报错

```
Model._train_process(self, epoch, train_dataset, list_callback, cb_params, initial_epoch, valid_infos)
    912 list_callback.on_train_step_begin(run_context)
    913 self._check_network_mode(self._train_network, True)
--> 914 outputs = self._train_network(*next_element)
```

检查是否忘记将输出标签也做数据转化

### image, label = next(train_dataset.create_tuple_iterator()) 报错

该行是让数据生成器产生一个值来激活生成器，如果报错，说明数据构造出现了问题