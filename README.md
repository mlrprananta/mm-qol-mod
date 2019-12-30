# QOL Mod by LuckyGlues
- Optimal car setup range indicator has been narrowed
- Tyre wear percentage indicator is now 0% when tyres start to cliff
- Finished part improvement and part repairs will interrupt game time
- Tyre temperature needle indicator is now red when overheating and underheating

Changes were made in the following classes and methods:

``` c#
public class DriverWidget : MonoBehaviour {
    private void UpdateTyreTemperature();
    private void UpdateTyreWear();
}

public class PartImprovement {
    private void SetEndDate(CarPartStats.CarPartStat inStackType)
}

public class SetupPerformance : PerformanceImpact {
    public void GetVisualKnowledgeRangeFromNormalisedValue(float inKnowledgeNormalised, out float[] outMinVisualOffset, out float[] outMaxVisualOffset);
}

public class TyreSet {
    public string GetConditionText();
    public void SetCondition(float inCondition);
}

public class UIDriverInfo : MonoBehaviour {
    private void Update();
}
```
