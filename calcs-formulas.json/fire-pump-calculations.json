{
  "topic": "Fire Pump Calculations",
  
  "overview": "Field calculations and guidelines for fire pump installations, focusing on motor sizing, conductor selection, voltage drop, and circuit protection. Complies with NFPA 20, NFPA 25, and NEC Article 695.",
  
  "calculations": {
    "formulas": {
      "basic_fire_pump": "EP = NP + FL + APP + ELEV (where EP = Engine Power, NP = Nominal Power, FL = Friction Loss, APP = Apparatus Flow, ELEV = Elevation)",
      "conductor_sizing": "Minimum Conductor Ampacity = FLA × 1.25 (per NEC Article 695)",
      "voltage_drop": {
        "starting": "Maximum 15% voltage drop at controller terminals during motor start",
        "running": "Maximum 5% voltage drop at motor terminals when operating at 115% of full load current",
        "three_phase": "Vdrop = 1.73 × Z × I × L ÷ 1000",
        "variables": "Z = line impedance (Ω/1000 ft), I = current (A), L = length (ft)"
      }
    },

    "tables": {
      "motor_fla": {
        "description": "Full Load Amps (FLA) for 3-phase fire pump motors. Always verify against nameplate data.",
        "data": {
          "headers": ["HP", "230V", "460V", "575V"],
          "values": [
            ["1", "4.2", "2.1", "1.7"],
            ["2", "6.0", "3.0", "2.4"],
            ["3", "8.4", "4.2", "3.4"],
            ["5", "13.8", "6.9", "5.5"],
            ["7.5", "20", "10", "8"],
            ["10", "28", "14", "11"]
          ]
        }
      }
    },

    "field_steps": [
      "1. Verify motor HP and voltage from nameplate",
      "2. Determine FLA from nameplate (not table)",
      "3. Calculate minimum conductor size (FLA × 1.25)",
      "4. Verify voltage drop limits:",
      "   - Max 15% at controller during start",
      "   - Max 5% at motor at 115% load",
      "5. Size overcurrent protection per NFPA 20"
    ],

    "example": {
      "scenario": "50HP fire pump motor at 460V",
      "steps": [
        "1. FLA from nameplate = 65A",
        "2. Minimum wire size = 65A × 1.25 = 81.25A",
        "3. Check voltage drop at start and run conditions",
        "4. Size overcurrent protection per NFPA 20 specific requirements"
      ]
    }
  },

  "key_points": {
    "installation": {
      "power_supply": [
        "Dedicated electrical service required (NEC 695)",
        "Proper overcurrent protection per NFPA 20",
        "Emergency power must meet same requirements as primary"
      ],
      "location": [
        "Disconnect in/near pump room",
        "Lockable in 'ON' position",
        "Clear access maintained"
      ]
    },

    "testing": {
      "requirements": {
        "monthly": [
          "No-flow test (churn)",
          "Record voltage/current",
          "Check controller status"
        ],
        "annual": [
          "Full flow test",
          "Document all readings",
          "Verify alarm functions"
        ],
        "references": "Per NFPA 20 and NFPA 25"
      }
    },

    "critical_notes": [
      "Always use nameplate FLA for final sizing",
      "Account for both starting and running voltage drop limits",
      "Follow specific NFPA 20 requirements for overcurrent protection",
      "Maintain test records on site",
      "Ensure proper room ventilation"
    ]
  }
}