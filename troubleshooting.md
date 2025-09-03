---
title: Troubleshooting Guide
layout: default
nav_order: 80
---

# Troubleshooting Guide
{: .no_toc }

Common problems and solutions for robotics projects. When something isn't working, start here to diagnose and fix issues quickly.

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Hardware Issues

### Robot Won't Turn On
**Symptoms**: No lights, no response to buttons
- **Check battery**: Is it charged? Properly connected?
- **Check power switch**: Is it in the ON position?
- **Check connections**: Are all cables firmly seated?
- **Try different battery**: Batteries can fail suddenly

### Motors Not Working
**Symptoms**: Robot doesn't move despite code running
- **Check motor connections**: Red to positive, black to negative
- **Verify ports**: Motors connected to correct brain ports?
- **Test motor power**: Try a simple test program
- **Check for binding**: Can wheels turn freely by hand?

### Sensors Not Responding
**Symptoms**: Sensor readings are always 0 or max value
- **Check wiring**: 3-wire sensors need power, ground, and signal
- **Verify port assignment**: Code matches physical connection?
- **Test sensor isolation**: Disconnect and test individually
- **Check for interference**: Keep sensor wires away from motors

---

## Programming Issues

### Code Won't Download
**Symptoms**: Error messages during download process
- **Check USB connection**: Try different cable or port
- **Brain connection**: Is the brain icon green in VEXcode?
- **Restart software**: Close and reopen VEXcode
- **Update firmware**: Brain and controller may need updates

### Robot Behaves Erratically
**Symptoms**: Unpredictable movement or sensor readings
- **Add delays**: `wait(20)` between loop iterations
- **Check variable scope**: Are variables initialized properly?
- **Debug with print**: Add screen output to see values
- **Simplify code**: Test one feature at a time

### Infinite Loops or Freezing
**Symptoms**: Robot stops responding, code doesn't advance
- **Add exit conditions**: Every loop needs a way out
- **Check while conditions**: Do they actually change?
- **Use print statements**: Track where code gets stuck
- **Add timeout limits**: Prevent endless waiting

---

## Electronics Issues

### LED Strip Not Working
**Symptoms**: No colors, wrong colors, or flickering
- **Check power**: LEDs need adequate current supply
- **Verify connections**: Data pin to correct micro:bit pin
- **Test simple pattern**: Start with solid colors
- **Check LED count**: Code matches actual LED quantity?

### Breadboard Circuits
**Symptoms**: Components don't work as expected
- **Check power rails**: Are positive/negative connected?
- **Verify connections**: Components share rows correctly?
- **Look for loose wires**: Push all connections firmly
- **Check component orientation**: LEDs, diodes have polarity

---

## Competition Robot Issues

### Sumo Robot Problems
**Symptoms**: Falls off platform, doesn't find opponents

#### Edge Detection Issues
- **Sensor height**: Too high/low to detect white line?
- **Ambient light**: Room lighting affects sensors
- **Calibration**: Run sensor calibration routine
- **Threshold values**: Adjust light/dark detection levels

#### Movement Problems
- **Speed too fast**: Robot can't react to sensors quickly
- **Turning radius**: Adjust to stay within ring boundaries
- **Weight distribution**: Heavy front helps with pushing
- **Wheel traction**: Clean wheels, check for wear

### Freeze Tag Robot Problems
**Symptoms**: Poor maneuvering, can't avoid obstacles

#### Control Responsiveness
- **Smoothing factor**: Balance stability vs. responsiveness
- **Speed limits**: Too fast = hard to control precisely
- **Controller deadzone**: Small joystick movements ignored
- **Battery level**: Low power affects motor performance

---

## Debugging Strategies

### Systematic Approach
1. **Isolate the problem**: What specific part isn't working?
2. **Start simple**: Test basic functionality first
3. **Change one thing**: Don't modify multiple things at once
4. **Document changes**: Keep track of what you've tried
5. **Ask for help**: Get fresh eyes on the problem

### Useful Debug Techniques

#### Visual Feedback
```python
# Add to your code to see variable values
brain.screen.clear_screen()
brain.screen.print("Sensor: {}".format(sensor_value))
brain.screen.print("Motor: {}".format(motor_speed))
```

#### Step-by-Step Testing
```python
# Test components individually
motor_left.set_velocity(50)
wait(1000)  # Run for 1 second
motor_left.stop()
```

#### Boundary Checking
```python
# Ensure values stay within expected ranges
if sensor_value < 0:
    sensor_value = 0
elif sensor_value > 100:
    sensor_value = 100
```

---

## Getting Help

### Self-Help Checklist
- [ ] Read error messages carefully
- [ ] Check physical connections
- [ ] Try a simpler version of your code
- [ ] Look for similar problems in documentation
- [ ] Test individual components separately

### When to Ask for Help
- **After trying basics**: Don't give up too quickly, but don't waste hours either
- **With specific questions**: "My motor won't turn" vs "nothing works"
- **With error messages**: Copy exact error text
- **During peer review**: Sometimes a teammate spots the issue immediately

### How to Ask for Help
1. **Describe the expected behavior**: What should happen?
2. **Explain the actual behavior**: What actually happens?
3. **List what you've tried**: Shows your problem-solving effort
4. **Share relevant code**: Only the part that's not working
5. **Mention recent changes**: What was the last thing that worked?

---

## Prevention Tips

### Best Practices
- **Save working versions**: Before making big changes
- **Test incrementally**: Add one feature at a time
- **Use clear variable names**: `left_motor_speed` vs `x`
- **Comment your code**: Explain complex logic
- **Keep backups**: Save multiple versions of working code

### Common Mistakes to Avoid
- **Forgetting to download**: Code changes don't apply until downloaded
- **Wrong port assignments**: Double-check physical vs. code connections
- **Missing delays**: Real-time systems need time between operations
- **Assuming sensors work**: Always test and calibrate sensors first
- **Ignoring battery level**: Low batteries cause mysterious problems

---

Remember: Every expert was once a beginner who encountered these same problems. Debugging skills improve with practice, and every problem solved makes you a better roboticist!