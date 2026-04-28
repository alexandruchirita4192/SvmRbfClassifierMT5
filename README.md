# SVM RBF MT5 strategy

## Algorithm
Support Vector Machine (SVC) with RBF kernel

- Non-linear classifier
- Uses distance-based decision boundary
- Sensitive to scaling (StandardScaler used)

## Run training

```text
python train_mt5_svm_rbf_classifier_scale_invariant.py --symbol XAGUSD --timeframe M15 --bars 80000 --horizon-bars 8 --train-ratio 0.82 --output-dir output_svm_rbf_XAGUSD_M15_h8_82
```
### Warning: SVM RBF training took few hours, this is the most time required by any algorithm until now to train an ONNX and produces few transactions.

## Files generated

- ml_strategy_classifier_svm_rbf.onnx
- model_metadata.json
- run_in_mt5.txt

## MT5 steps

1. Copy ONNX near EA
2. Recompile EA
3. Use TEST window from run_in_mt5.txt

## Notes

- Requires feature scaling
- More sensitive than tree models
- Usually produces more trades than GMM
