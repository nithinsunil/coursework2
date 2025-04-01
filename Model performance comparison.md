- Model Performance Comparison

| Model                       | MAE (Lower Better) | RMSE (Lower Better) | R² (Higher Better) |
| --------------------------- | ------------------ | ------------------- | ------------------ |
| XGBoost (All Features)      | 14,286.72          | 23,983.23           | 0.928              |
| LightGBM (All Features)     | 15,331.89          | 26,107.86           | 0.915              |
| Random Forest (No Location) | 15,706.00          | 26,671.00           | 0.911              |

---

- Key Conclusions

1. XGBoost is the Clear Winner

   - 7.3% more accurate than LightGBM (MAE: 14,287 vs 15,332)
   - 9.3% lower error than Random Forest (RMSE: 23,983 vs 26,671)
   - Best explains price variance (R² 0.928 vs 0.915/0.911)

2. Performance Hierarchy  
   XGBoost > LightGBM > Random Forest  
   (All metrics consistently agree on this ranking)

3. Practical Implications
   - Using XGBoost could save $1,045 per prediction vs LightGBM (MAE difference)
   - For a $300K home XGBoost's predictions are typically within ±$14.3K vs LightGBM's ±$15.3K

---

- Why XGBoost Outperforms

| Factor               | XGBoost Advantage                                                                                    |
| -------------------- | ---------------------------------------------------------------------------------------------------- |
| Feature Interactions | Better captures nonlinear relationships (e.g., how quality and neighborhood combine to affect price) |
| Regularization       | More resistant to overfitting on small datasets                                                      |
| Error Correction     | Iteratively fixes residual errors more effectively                                                   |
| Implementation       | Optimized for single-machine performance                                                             |

---

- Recommendation

1. Production Deployment: Use XGBoost with all features for most accurate predictions
2. Model Monitoring: Track if errors increase for luxury homes (>$400K)
3. Future Improvements:
   - Add more luxury home samples to improve high-end predictions
   - Test feature interactions (e.g., `Overall Qual × Neighborhood`)
