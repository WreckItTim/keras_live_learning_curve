# keras_live_learning_curve
Simple allback to add to keras model that outputs live updated learning curve!
Better than verbose text output in my opinion, just copy and paste code.

Use by adding callback to callbacks list in model fit, such as:
model.fit(callbacks=[learning_curve(), ..., ])

Just copy and paste below code and use:

class learning_curve(tf.keras.callbacks.Callback):
    def __init__(self):
        self.epochs = []
        self.losses = []
    def on_epoch_end(self, epoch, logs=None):
        clear_output(wait=True)
        self.epochs.append(len(self.epochs))
        self.losses.append(logs.get('loss'))
        plt.plot(self.epochs, self.losses)
        plt.title('Learning Curve')
        plt.xlabel('Epoch')
        plt.ylabel('Loss')
        plt.show()
