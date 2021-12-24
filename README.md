# keras_live_learning_curve
Simple callback to add to keras model that outputs live updated learning curve!
Better than verbose text output in my opinion, just copy and paste code.

Use by setting verbose=0 and adding callback to callbacks list in model fit, such as:
model.fit(callbacks=[learning_curve(), ..., ], verbose=0)
