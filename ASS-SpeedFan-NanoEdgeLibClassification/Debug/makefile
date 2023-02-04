################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (10.3-2021.10)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32L4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := ASS-SpeedFan-NanoEdgeLibClassification
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
ASS-SpeedFan-NanoEdgeLibClassification.elf \

MAP_FILES += \
ASS-SpeedFan-NanoEdgeLibClassification.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
ASS-SpeedFan-NanoEdgeLibClassification.list \


# All Target
all: main-build

# Main-build Target
main-build: ASS-SpeedFan-NanoEdgeLibClassification.elf secondary-outputs

# Tool invocations
ASS-SpeedFan-NanoEdgeLibClassification.elf ASS-SpeedFan-NanoEdgeLibClassification.map: $(OBJS) $(USER_OBJS) C:\Users\60111\STM32CubeIDE\workspace_1.10.1\ASS-SpeedFan-NanoEdgeLibClassification\STM32L432KCUX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "ASS-SpeedFan-NanoEdgeLibClassification.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\60111\STM32CubeIDE\workspace_1.10.1\ASS-SpeedFan-NanoEdgeLibClassification\STM32L432KCUX_FLASH.ld" --specs=nosys.specs -Wl,-Map="ASS-SpeedFan-NanoEdgeLibClassification.map" -Wl,--gc-sections -static -L"C:\Users\60111\STM32CubeIDE\workspace_1.10.1\ASS-SpeedFan-NanoEdgeLibClassification\acc_lib" -u_printf_float --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

ASS-SpeedFan-NanoEdgeLibClassification.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "ASS-SpeedFan-NanoEdgeLibClassification.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) ASS-SpeedFan-NanoEdgeLibClassification.elf ASS-SpeedFan-NanoEdgeLibClassification.list ASS-SpeedFan-NanoEdgeLibClassification.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
