{
  "Elevators_and_Escalators": {
    "overview": {
      "description": "Elevator and escalator electrical systems demand specialized considerations for power supply reliability, emergency operations, and safety. Strict code provisions govern normal and emergency operating conditions, ensuring continuous service and passenger protection.",
      "key_focus_areas": [
        "Power quality management and monitoring",
        "Comprehensive backup power systems",
        "Safety interlocks and emergency operations",
        "Maintenance accessibility requirements"
      ]
    },
    "power_requirements": {
      "essential_formulas": {
        "branch_circuit_sizing": {
          "main_power": "Branch circuit sizing at 125% of the nameplate full load current (FLA) with additional consideration for starting current per NEC Article 430.52(B).",
          "control_circuits": "Control circuits sized per manufacturer's or code-based recommendations.",
          "lighting_auxiliary": "Separate branch circuits required for elevator car lighting, ventilation, and other auxiliary loads."
        },
        "voltage_drop": {
          "maximum_starting": "Up to 15% during motor starting conditions (peak inrush).",
          "normal_operation": "Within 5% of nominal voltage under steady-state operation.",
          "calculation_basis": "Based on maximum conductor run length from the distribution source."
        },
        "emergency_power": {
          "sizing_basis": "Must accommodate the largest elevator group running simultaneously.",
          "auxiliary_systems": "Include power for lighting (Type 10, Class 1.5, Level 1), ventilation, and door control.",
          "starting_requirements": "Account for total inrush current when sizing backup systems.",
          "classification": "Elevators classified as Type 60, Level 2 systems per NFPA 110"
        }
      },
      "calculation_steps": [
        {
          "step": "Total Connected Load Assessment",
          "details": [
            "Sum all elevator motor loads (traction, hydraulic, door motors).",
            "Include auxiliary loads such as car lighting, HVAC, and controls.",
            "Factor in requirements for simultaneous operation of multiple cars."
          ]
        },
        {
          "step": "Demand Factor Application",
          "details": [
            "Apply occupancy-specific demand factors (e.g., high-rise, commercial).",
            "Consider building peak usage periods (rush hours).",
            "Evaluate emergency scenarios that might require multiple cars in use."
          ]
        },
        {
          "step": "Emergency Power Sizing",
          "details": [
            "Ensure capacity for simultaneous operation of the largest group of cars.",
            "Include essential auxiliary loads (lighting, ventilation, control circuits).",
            "Confirm required minimum runtime (per AHJ or manufacturer guidelines)."
          ]
        },
        {
          "step": "Voltage Drop Verification",
          "details": [
            "Calculate maximum voltage drop during starting conditions.",
            "Confirm that normal operation voltage remains within 5% nominal.",
            "Maintain records of calculations for code inspections and commissioning."
          ]
        }
      ]
    },
    "emergency_power_requirements": {
      "building_types": {
        "high_rise": {
          "requirement": "All elevators except those in R-2 occupancies, per local code.",
          "notes": "Consult AHJ for variations in high-rise definitions."
        },
        "r2_over_125ft": {
          "requirement": "At least one elevator must be on emergency backup.",
          "notes": "Elevator must serve all floors above 125 ft."
        },
        "underground": {
          "requirement": "All elevators require emergency power backup.",
          "notes": "Include ventilation systems for each elevator and hoistway."
        },
        "healthcare": {
          "requirement": "Selected cars (often at least one) for patient transport and emergency use.",
          "notes": "Coordinate with the facility's overall emergency plan."
        }
      }
    },
    "code_compliance": {
      "nec_article_620": {
        "installation_requirements": [
          "GFCI protection for all 125 V receptacles within pits and machinery spaces.",
          "Separate branch circuit(s) required for pit lighting and receptacles.",
          "Elevator disconnects must be lockable in the open position only.",
          "Equipment grounding conductor required in all raceways and cables."
        ],
        "accessibility_safety": [
          "A dedicated disconnect must be readily accessible for each elevator or escalator.",
          "Maintenance disconnect required in machinery spaces (NEC 620).",
          "Sufficient working space around electrical equipment must be maintained.",
          "All equipment must be clearly labeled and identified per code."
        ]
      },
      "circuit_protection": {
        "overcurrent_protection": {
          "circuit_breakers": "Maximum 250% of FLA per Table 430.52",
          "fuses": "Maximum 175% of FLA per Table 430.52",
          "example": {
            "motor_specs": "15HP elevator with 48A FLA",
            "fused_disconnect": "84A (48A × 1.75)",
            "circuit_breaker": "120A (48A × 2.5)"
          }
        }
      },
      "accessibility": {
        "egress_requirements": {
          "application": "Required when four or more stories above/below exit discharge level",
          "power_requirements": [
            "Must have standby power source",
            "Emergency generator required (battery backup not sufficient)"
          ]
        }
      },
      "emergency_systems": {
        "power_transfer": {
          "activation_time": "Must activate within 60 seconds of normal power loss.",
          "requirements": [
            "Automatic transfer switch (ATS) typically required.",
            "Regular testing and maintenance per NFPA 110 or local standards."
          ]
        },
        "essential_functions": [
          "Car lighting, ventilation, and door operation must remain powered.",
          "Emergency communication systems (phones, intercoms) require backup.",
          "Environmental controls (machine room cooling) must be maintained if specified."
        ]
      }
    },
    "practical_implementation": {
      "machine_room": {
        "requirements": [
          "Ventilation/cooling systems must have backup power (if required by code).",
          "Elevator lighting circuits must not be downstream of pit GFCIs.",
          "Maintain minimum lighting levels (often 10 fc or per local standard).",
          "Consider temperature/humidity monitoring for sensitive control equipment."
        ]
      },
      "pit_hoistway": {
        "requirements": [
          "Both lighting and GFCI protection are required in the pit area.",
          "Locate disconnects for easy accessibility and safe lockout.",
          "Use a separate circuit for sump pumps (if installed).",
          "Seal openings or penetrations to maintain fire-rated integrity."
        ]
      }
    },
    "example_calculations": {
      "building_spec": {
        "type": "Commercial",
        "stories": 6,
        "elevators": {
          "count": 3,
          "power": "40 HP each"
        }
      },
      "calculations": {
        "base_load": {
          "elevator_motors": "111.9 kW (3 × 40 HP × 746 W/HP × 125% factor)",
          "auxiliary_loads": "5 kW (lighting, HVAC, controls, etc.)",
          "total_connected": "116.9 kW"
        },
        "emergency_power": {
          "largest_group": "2 elevators running simultaneously",
          "required_capacity": "154.2 kW ((74.6 kW × 2) + 5 kW)",
          "with_safety_factor": "185 kW minimum (includes a ~20% margin)"
        }
      }
    },
    "important_notes": [
      "Always verify specific requirements with the local Authority Having Jurisdiction (AHJ).",
      "Consult manufacturer specifications and NEC references for precise requirements.",
      "Document all calculations, assumptions, and design decisions for inspections.",
      "Maintain updated emergency procedures, including transfer and startup protocols."
    ]
  }
}