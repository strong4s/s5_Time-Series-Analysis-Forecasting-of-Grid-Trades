Files Directory
* Files are from joblib UNLESS specified as .csv

====================================================================

_df == Orig | Upon read & concat
_df2 == From _df | Feat. Eng'g., imputed 2015 | MAJOR change: Added _pt.

_df_enr == [Jul 7] | From _df2 | Obj: Still contains the orig features. | Specified End Time on >= 2016 | used in n2
_df_sys == [Jul 7] | From _df2 | Obj: Still contains the orig features. | Specified End Time on >= 2016 | used in n2

df_sysD_19-21.csv = From _df_enr | Dtale, omitted 2018 & older | Used in N3
df_enrD_19-21.csv = From _df_sys | Dtale, omitted 2018 & older | Used in N3

_df_enrD_19-21 = From df_sysD_19-21.csv | Before formatting "End Time_" as datetime
_df_enrD_19-21 = From df_sysD_19-21.csv | Before formatting "End Time_" as datetime



=============FOR==DELETION===========================================

_df_enr_M_1920 == From _df_enr | Trimmed from 2019 - 2020, as Training for ARIMA | Deletion: Widening dataset for N4, not limiting to 2019 onwards
_df_enr_M_21 == From _df_enr | 2021, as Test for ARIMA | Deletion: Widening dataset for N4, not limiting to 2019 onwards


_df1A == PREVIOUSLY manipulated & feat. eng'g dataset.
        From Old TSA

_Energy Trades Cost_df3A == From _df1A. Only Cost remaining. Prev. used in N3
_Energy Trades Cost_df4A == From _df1A. Only Cost remaining. Prev. used in N3

====================================END==============================
