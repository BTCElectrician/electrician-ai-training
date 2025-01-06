{
  "topic": "Power Factor & Harmonics",
  
  "overview": "Essential calculations and guidelines for power factor correction and harmonic mitigation in electrical systems. Includes capacitor sizing, harmonic analysis, and equipment selection strategies to maintain and improve power quality.",
  
  "calculations": {
    "formulas": {
      "power_factor": {
        "basic": "Power Factor (PF) = True Power (kW) / Apparent Power (kVA). PF typically ranges between 0 and 1.",
        "capacitor_sizing": "Required Capacitor (kVAR) = P × (tan φ1 – tan φ2), where P is load in kW, φ1 is the existing power factor angle, and φ2 is the target power factor angle.",
        "thd": "Total Harmonic Distortion (THD) = √[Σ(Vh²) / V1²] × 100%, measuring the overall harmonic content in the voltage waveform.",
        "individual_harmonic": "Individual Harmonic Distortion (IHD) = (Ih / I1) × 100%, where Ih is the harmonic current at a given order h, and I1 is the fundamental current.",
        "k_factor": "K-Factor = Σ(Ih² × h²). Higher K-Factors indicate heavier harmonic loading, requiring specialized transformers."
      },
      
      "steps": [
        "1. Measure existing power factor, load kW, and harmonic levels.",
        "2. Determine target power factor (commonly 0.95-0.98).",
        "3. Calculate required capacitor sizing (kVAR) using a known multiplier or the tan φ method.",
        "4. Measure/estimate THD and identify dominant harmonic orders (3rd, 5th, 7th, 11th, etc.).",
        "5. Select appropriate harmonic mitigation equipment based on the harmonic profile (passive/active filters, K-rated transformers, etc.)."
      ]
    },
    
    "tables": {
      "pf_correction_multipliers": {
        "description": "Multipliers for calculating required capacitor kVAR (Required kVAR = kW × multiplier). These values assume typical load characteristics. Adjust if necessary for site-specific conditions.",
        "example": "For a 600 kW load at 75% PF corrected to 95% PF: Required kVAR = 600 × 0.553 = 331.8 kVAR",
        "data": {
          "0.70_to_0.95": "0.691",
          "0.75_to_0.95": "0.553",
          "0.80_to_0.95": "0.421",
          "0.85_to_0.95": "0.291",
          "0.90_to_0.95": "0.168"
        }
      },
      
      "k_factor_selection": {
        "description": "Common UL-listed K-Factor ratings for transformers under various non-linear load conditions. Higher K-Factors accommodate heavier harmonic currents.",
        "data": {
          "K4": [
            "Electric lighting with non-linear ballasts",
            "Welding equipment",
            "UPS with input filters"
          ],
          "K13": [
            "UPS without input filters",
            "Telecommunications equipment",
            "General office areas with varied IT loads"
          ],
          "K20": [
            "Data centers and server rooms",
            "Variable Frequency Drives (VFDs)",
            "Large computer or laboratory loads"
          ]
        }
      },
      
      "harmonic_limits": {
        "voltage": {
          "description": "IEEE Std 519 voltage distortion limits at various voltage levels.",
          "data": {
            "LV": "8% (Low Voltage < 1 kV)",
            "MV": "6.5% (Medium Voltage 1 kV–69 kV)",
            "HV": "3% (High Voltage > 69 kV)"
          }
        },
        "current": {
          "description": "Typical maximum harmonic current distortion limits in percent of fundamental current (IEEE Std 519).",
          "data": {
            "3rd_to_9th": "4%",
            "11th_to_15th": "2%",
            "17th_to_21st": "1.5%",
            "23rd_to_33rd": "0.6%",
            "35th_and_above": "0.3%",
            "TDD_limit": "5% (Total Demand Distortion)"
          }
        }
      },
      
      "transformer_derating": {
        "factors": {
          "single_phase_supplies": "Recommend 30-40% capacity margin for single-phase non-linear loads.",
          "thd_above_5%": "Consider 20% additional capacity for THD above 5%."
        },
        "mitigation_options": [
          "Use K-rated transformer (K4, K13, K20, etc.)",
          "Apply derating factor to standard transformers",
          "Implement passive or active harmonic filtering"
        ]
      }
    }
  },
  
  "key_considerations": {
    "code_requirements": {
      "ieee_519": "Establishes recommended limits for harmonic voltages and currents to maintain power quality.",
      "nec_460": "Covers capacitor installation requirements (overcurrent protection, disconnecting means, etc.).",
      "ul_1561": "Standard for dry-type general-purpose and power transformers, including safety provisions."
    },
    
    "practical_notes": [
      "Install PF correction capacitors upstream of VFDs to avoid resonance and overvoltage issues.",
      "Active harmonic filters can be more effective when multiple non-linear loads are present.",
      "Avoid over-correction of power factor at light loads (risk of leading PF).",
      "Include generator operation in harmonic and PF correction design (generator reactance differs from utility).",
      "Monitor neutral conductor loading in three-phase systems with high triplen (3rd, 9th) harmonics.",
      "Locate correction equipment close to the largest loads, if possible, to minimize wiring and losses.",
      "Always account for ambient temperature and ventilation when installing capacitor banks."
    ],
    
    "common_issues": {
      "resonance": "Occurs between capacitors and system inductance, potentially amplifying harmonic currents.",
      "overheating": "Elevated harmonic currents cause additional heat in transformers, cables, and motors.",
      "nuisance_tripping": "High harmonic levels can trigger protective devices improperly.",
      "voltage_distortion": "May affect sensitive electronic equipment such as PLCs, robotics, and instrumentation.",
      "neutral_overload": "Triplen harmonics (3rd, 9th, 15th) sum in the neutral conductor, creating overload risks."
    },
    
    "safety": [
      "All capacitors must include discharge resistors/mechanisms for safe de-energization.",
      "Excessive harmonic currents lead to overheating and possible equipment failure. Monitor regularly.",
      "Use properly rated PPE (arc flash gear, etc.) when inspecting, installing, or servicing capacitors.",
      "Verify proper discharge of capacitor banks before maintenance or inspection.",
      "Follow arc flash safety protocols per NFPA 70E for all energized or potentially energized equipment."
    ]
  },
  
  "equipment_selection": {
    "capacitor_banks": {
      "fixed": "Suitable for relatively steady loads with minor fluctuations in PF requirements.",
      "automatic": "Equipped with contactors or thyristor controls for varying loads and precise PF correction.",
      "considerations": [
        "Voltage rating (must exceed system operating voltage + margin)",
        "Current rating (inrush and harmonic components)",
        "Discharge time (often required to be under 1 minute)",
        "Environmental conditions (temperature, humidity, dust)",
        "Control method (step switching, thyristor-based, etc.)"
      ]
    },
    
    "harmonic_mitigation": {
      "passive_filters": "Tuned filters that target one or more specific harmonic frequencies. Effective but size-sensitive.",
      "active_filters": "Provide real-time mitigation for multiple harmonic orders. More flexible, generally higher cost.",
      "k_rated_transformers": "Built with lower losses and heavier winding designs to handle high harmonic content.",
      "selection_criteria": [
        "Harmonic spectrum analysis (identify dominant orders)",
        "Overall load profile (intermittent vs. continuous non-linear loads)",
        "Cost considerations (initial vs. life-cycle cost)",
        "Space constraints (footprint for filters, clearances)",
        "Maintenance requirements (active filters require more monitoring)"
      ]
    }
  }
}
