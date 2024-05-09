################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (10.3-2021.10)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/W5500/W5500/subdir.mk
-include Core/W5500/subdir.mk
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


BUILD_ARTIFACT_NAME := WIZ5500_SNTP_RTC_STM32C6T6
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
WIZ5500_SNTP_RTC_STM32C6T6.elf \

MAP_FILES += \
WIZ5500_SNTP_RTC_STM32C6T6.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
WIZ5500_SNTP_RTC_STM32C6T6.list \


# All Target
all: main-build

# Main-build Target
main-build: WIZ5500_SNTP_RTC_STM32C6T6.elf secondary-outputs

# Tool invocations
WIZ5500_SNTP_RTC_STM32C6T6.elf WIZ5500_SNTP_RTC_STM32C6T6.map: $(OBJS) $(USER_OBJS) C:\Embedded-C\Personal_course\Stm32_Excercise\WIZ5500_SNTP_RTC_STM32C6T6\STM32F103C6TX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "WIZ5500_SNTP_RTC_STM32C6T6.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Embedded-C\Personal_course\Stm32_Excercise\WIZ5500_SNTP_RTC_STM32C6T6\STM32F103C6TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="WIZ5500_SNTP_RTC_STM32C6T6.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

WIZ5500_SNTP_RTC_STM32C6T6.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "WIZ5500_SNTP_RTC_STM32C6T6.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) WIZ5500_SNTP_RTC_STM32C6T6.elf WIZ5500_SNTP_RTC_STM32C6T6.list WIZ5500_SNTP_RTC_STM32C6T6.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
