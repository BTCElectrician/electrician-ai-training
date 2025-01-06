{
  "Renewable_Power_Systems": {
    "overview": {
      "description": "Renewable energy systems, particularly solar PV, require specific electrical calculations and safety considerations for grid interconnection, power generation, and emergency shutdown. These systems must comply with both national standards and local requirements, particularly in urban environments like Chicago.",
      "key_focus_areas": [
        "Power quality management and monitoring",
        "Comprehensive backup power systems",
        "Safety interlocks and emergency operations",
        "Maintenance accessibility requirements",
        "Local code compliance and utility interconnection",
        "Climate-specific structural considerations"
      ]
    },
    "power_requirements": {
      "essential_formulas": {
        "system_sizing": {
          "annual_energy": "Annual Energy Output (kWh) = Pr × H × PR",
          "inverter_ratio": "Inverter Sizing Ratio = DC Array Rating / Inverter AC Rating",
          "performance_ratio": "Performance Ratio (PR) = System Efficiency × Inverter Efficiency × Loss Factors",
          "array_size": "Solar Array Size (kW) = Daily Load (kWh) / Solar Irradiance (kWh/m²)",
          "snow_load": "Snow Load = Ground Snow Load × Exposure Factor × Thermal Factor × Importance Factor"
        },
        "voltage_considerations": {
          "maximum_starting": "Up to 15% during motor starting conditions (peak inrush)",
          "normal_operation": "Within 5% of nominal voltage under steady-state operation",
          "rapid_shutdown": "Must reduce to 30V or less within 30 seconds"
        }
      },
      "calculation_steps": [
        {
          "step": "Total Connected Load Assessment",
          "details": [
            "Calculate total solar capacity needed",
            "Factor in local climate conditions and shading",
            "Account for system losses and derating factors"
          ]
        },
        {
          "step": "Environmental Factors",
          "details": [
            "Account for Chicago snow loads (40-100 lbs/sq ft)",
            "Consider wind load requirements",
            "Factor in temperature effects on performance"
          ]
        },
        {
          "step": "Safety System Sizing",
          "details": [
            "Design rapid shutdown compliance",
            "Size disconnecting means appropriately",
            "Plan emergency access routes"
          ]
        }
      ]
    },
    "chicago_specific_requirements": {
      "electrical_code": {
        "base_code": "2017 NEC with Chicago amendments",
        "key_modifications": {
          "article_690": "Revision to 690.7(A) removing item (3)",
          "rapid_shutdown": {
            "voltage_requirement": "30 volts or less within 30 seconds",
            "controlled_conductors": "Within 1 foot of PV array",
            "labeling": "Permanent label required per Chicago Fire Prevention Code"
          }
        }
      },
      "structural": {
        "solar_ready_requirements": {
          "building_criteria": "7,500 sq. ft. footprint, height ≤ 60 feet",
          "zone_requirement": "40% of roof area",
          "load_design": "Minimum 5 lbs per sq. ft. additional dead load"
        },
        "snow_load": {
          "panel_capacity": "40-100 pounds per square foot",
          "coverage_period": "3-5 months annually"
        }
      },
      "fire_safety": {
        "access_pathways": {
          "width": "3-foot-wide clear access",
          "location": "From eave to ridge on each roof slope",
          "ridge_clearance": "3-foot clearance down from ridge"
        },
        "setbacks": {
          "ridge_line": "3 feet from any roof ridge line"
        }
      },
      "comed_interconnection": {
        "standards": {
          "base_standard": "IEEE 1547",
          "levels": [
            {
              "level": "Level 1",
              "size": "< 25 kW",
              "notes": "Lab-certified systems"
            }
          ]
        },
        "incentives": {
          "commercial": {
            "amount": "$250 per 1 kW installed",
            "limit": "Under 2000 kW"
          }
        }
      }
    },
    "commercial_systems": {
      "system_categories": {
        "small": {
          "size": "25-75 kW",
          "cost": "$50,000 - $100,000",
          "typical_application": "Small commercial buildings"
        },
        "medium": {
          "size": "100-200 kW",
          "cost": "$150,000 - $350,000",
          "typical_application": "Medium commercial facilities"
        },
        "large": {
          "size": "250-300 kW",
          "cost": "$400,000 - $600,000",
          "typical_application": "Large commercial buildings"
        }
      },
      "financing_options": {
        "c_pace": {
          "description": "Commercial Property Assessed Clean Energy financing",
          "coverage": "New construction, maintenance, upgrades"
        }
      }
    },
    "safety_compliance": {
      "disconnecting_means": {
        "quantity_limit": "Maximum 6 switches or circuit breakers per system",
        "requirements": [
          "Rated for maximum circuit current",
          "Rated for available fault current",
          "Rated for voltage at PV system terminals"
        ]
      },
      "emergency_systems": {
        "rapid_shutdown": {
          "activation": "Must activate within 30 seconds",
          "voltage_reduction": "To 30V or less",
          "labeling": "Permanent plaque or directory required"
        }
      }
    },
    "design_considerations": {
      "inverter_sizing": {
        "typical_ratio": "1.15-1.25 times AC output rating",
        "guide": {
          "2kW_system": "6-8 panels (300-400W each)",
          "3kW_system": "7-10 panels (330-400W each)",
          "5kW_system": "13 panels (400W each)"
        }
      },
      "practical_notes": [
        "Consider shading from surrounding buildings",
        "Account for roof age and condition",
        "Plan for maintenance access",
        "Factor in future expansion possibilities",
        "Consider building energy management integration"
      ]
    },
    "maintenance_requirements": {
      "regular_inspection": [
        "Annual system performance verification",
        "Electrical connection integrity checks",
        "Emergency systems testing",
        "Snow removal protocol implementation",
        "Documentation updates as required"
      ]
    }
  }
}