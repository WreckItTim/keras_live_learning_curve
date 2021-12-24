# keras_live_learning_curve
Simple allback to add to keras model that outputs live updated learning curve!
Better than verbose text output in my opinion, just copy and paste code.

Use by adding callback to callbacks list in model fit, such as:
model.fit(callbacks=[learning_curve(), ..., ])
