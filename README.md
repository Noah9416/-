# -
利用python脚本在模型训练代码中添加损失值记录
import csv
with open('training_log.csv', 'w') as f:
    writer = csv.writer(f)
    writer.writerow(['epoch', 'train_loss', 'val_mae'])
    for epoch in range(100):
        # ...训练代码...
        writer.writerow([epoch, loss.item(), val_mae])
