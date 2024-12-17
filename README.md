# GM_input_manager

## Functions in Input_manager.gml

### `init_input(input_array = [])`
Initializes the input controls. If a `controls.profile` file exists, it loads the input configuration; otherwise, it saves the provided `input_array` to a file. Debug messages are displayed for success or failure.

**Parameters:**
- `input_array` *(array)*: Default input configuration array.
Esach value should contain an array of inputs to check. Each value is equal to an action

### `input_check(index)`
Checks if an input at a specified index is currently active.

**Parameters:**
- `index` *(int)*: The index of the input to check.

**Returns:**
- `bool`: True if the input is active, otherwise false.

### `input_pressed(index)`
Checks if an input at a specified index has just been pressed.

**Parameters:**
- `index` *(int)*: The index of the input to check.

**Returns:**
- `bool`: True if the input was just pressed, otherwise false.

### `input_released(index)`
Checks if an input at a specified index has just been released.

**Parameters:**
- `index` *(int)*: The index of the input to check.

**Returns:**
- `bool`: True if the input was just released, otherwise false.

### `input_state_check(index, kb_function, gp_function)`
A helper function to check input states for both keyboard and gamepad inputs. It iterates through the input array and verifies the state of the specified inputs.

**Parameters:**
- `index` *(int)*: The index of the input to check.
- `kb_function` *(function)*: The keyboard check function.
- `gp_function` *(function)*: The gamepad button check function.

**Returns:**
- `bool`: True if the input condition is satisfied, otherwise false.

## Dependencies

This script has a dependency on `GM_filemanager` for handling file operations, such as reading and writing the `controls.profile` file.

All required files are included to ensure the input manager works seamlessly without additional configuration.
