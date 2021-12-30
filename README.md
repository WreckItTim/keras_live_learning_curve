# keras_live_learning_curve
Simple callback to add to keras model that outputs live updated learning curve!
Better than verbose text output in my opinion, just copy and paste code.


Use by setting verbose=0 and adding callback to callbacks list in model fit, such as:

model.fit(..., callbacks=[learning_curve(['loss', 'val_loss']), ..., ], verbose=0)


when initializing, select which metrics to track in learning curve (i.e. 'loss', 'val_loss', etc)


view example file for simple application on sklearn iris dataset
