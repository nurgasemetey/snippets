### pandas compare two columns


 [python - How to compare two columns of the same dataframe? - Stack Overflow](https://stackoverflow.com/questions/42405572/how-to-compare-two-columns-of-the-same-dataframe "python - How to compare two columns of the same dataframe? - Stack Overflow")


 

```
high_scores1['is_score_chased'] = np.where(high_scores1['runs1']>=high_scores1['runs2'], 
                                           'yes', 'no')
gdf_geometry_filtered["REGION_DIFFERENT"]= np.where(gdf_geometry_filtered['Kaza_İli_TR_CODE']==gdf_geometry_filtered['adm1'], 
                                           'NO', 'YES')

```
