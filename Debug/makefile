################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F0xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
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

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
throwaway_proj.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
throwaway_proj.list \

OBJCOPY_BIN += \
throwaway_proj.bin \


# All Target
all: throwaway_proj.elf secondary-outputs

# Tool invocations
throwaway_proj.elf: $(OBJS) $(USER_OBJS) /Users/Kefford/STM32CubeIDE/workspace_1.3.0/throwaway_proj/STM32F072RBTX_FLASH.ld
	arm-none-eabi-gcc -o "throwaway_proj.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0 -T"/Users/Kefford/STM32CubeIDE/workspace_1.3.0/throwaway_proj/STM32F072RBTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="throwaway_proj.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

throwaway_proj.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "throwaway_proj.list"
	@echo 'Finished building: $@'
	@echo ' '

throwaway_proj.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "throwaway_proj.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
