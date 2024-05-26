# Clock_with_Alarm

This Verilog project implements a digital clock with an alarm feature. It generates seven output signals including Alarm, Hour, Minute, and Second. The clock operates in a 24-hour format and allows setting the initial time and alarm time through input signals.

## Key Features

- **Clock Signals**: Generates 7 output signals including Alarm, Hour, Minute, and Second.
- **Initial Time Setting**: Set the initial time using the reset signal or LD_time activation.
- **Alarm Setting**: Set the alarm time using LD_alarm activation.
- **Alarm Control**: Toggle alarm functionality using AL_ON input; stop alarm using STOP_al signal.
- **Clock Generation**: Utilizes a 10Hz input clock to derive a 1-second clock signal.

## Input Signals

- `reset`: Active high reset pulse for setting time and alarm.
- `clk`: 10Hz input clock for real-time seconds.
- `H_in1`, `H_in0`, `M_in1`, `M_in0`: Inputs for hour and minute digits.
- `LD_time`: Sets time values when activated.
- `LD_alarm`: Sets alarm time values when activated.
- `STOP_al`: Stops the alarm when triggered.
- `AL_ON`: Toggles alarm functionality.

## Output Signals

- `Alarm`: High when alarm time matches current time and AL_ON is active.
- `H_out1`, `H_out0`, `M_out1`, `M_out0`, `S_out1`, `S_out0`: Hour, minute, and second digits.

## Internal Signals

- `clk_1s`: 1-second clock signal.
- `tmp_1s`: Counter for generating 1-second clock.
- `tmp_hour`, `tmp_minute`, `tmp_second`: Clock hour, minute, and second counters.
- `c_hour1`, `a_hour1`, `c_hour0`, `a_hour0`, `c_min1`, `a_min1`, `c_min0`, `a_min0`, `c_sec1`, `a_sec1`, `c_sec0`, `a_sec0`: Temporary clock and alarm digits.

## Tools Used

- **Verilog**: Hardware Description Language
- **Icarus Verilog**: For simulation
- **Git**: For version control

