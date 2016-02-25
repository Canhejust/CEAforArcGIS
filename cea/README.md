##Building Energy Simultion
Excecuted throught the `demand.py` file. Functions for this are in the `functions.py`

The main equations seem to be line 159 in `functions.py` however the mathamatical derivation needs to be requested

```def Calc_Tm(Htr_3,Htr_1,tm_t0,Cm,Htr_em,Im_tot,Htr_ms,I_st,Htr_w,te_t,I_ia,IHC_nd,Hve,Htr_is):
 
    tm_t = (tm_t0 *((Cm/3600)-0.5*(Htr_3+ Htr_em))+ Im_tot)/((Cm/3600)+0.5*(Htr_3+Htr_em)) 
    tm = (tm_t+tm_t0)/2
    ts = (Htr_ms * tm + I_st + Htr_w*te_t + Htr_1*(te_t+(I_ia+IHC_nd)/Hve))/(Htr_ms+Htr_w+Htr_1)
    ta = (Htr_is*ts + Hve*te_t + I_ia + IHC_nd)/(Htr_is+Hve)
    top = 0.31*ta+0.69*ts
    return tm, ts, ta, top```