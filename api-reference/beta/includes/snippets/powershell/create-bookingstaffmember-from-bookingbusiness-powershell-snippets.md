---
description: "Automatically generated file. DO NOT MODIFY"
---

```powershell

Import-Module Microsoft.Graph.Bookings

$params = @{
	"@odata.type" = "#microsoft.graph.bookingStaffMember"
	ColorIndex = 1
	DisplayName = "Dana Swope"
	EmailAddress = "danas@contoso.com"
	"Role@odata.type" = "#microsoft.graph.bookingStaffRole"
	Role = "externalGuest"
	TimeZone = "America/Chicago"
	UseBusinessHours = $true
	"WorkingHours@odata.type" = "#Collection(microsoft.graph.bookingWorkHours)"
	WorkingHours = @(
		@{
			"@odata.type" = "#microsoft.graph.bookingWorkHours"
			"Day@odata.type" = "#microsoft.graph.dayOfWeek"
			Day = "monday"
			"TimeSlots@odata.type" = "#Collection(microsoft.graph.bookingWorkTimeSlot)"
			TimeSlots = @(
				@{
					"@odata.type" = "#microsoft.graph.bookingWorkTimeSlot"
					End = "17:00:00.0000000"
					Start = "08:00:00.0000000"
				}
			)
		}
		@{
			"@odata.type" = "#microsoft.graph.bookingWorkHours"
			"Day@odata.type" = "#microsoft.graph.dayOfWeek"
			Day = "tuesday"
			"TimeSlots@odata.type" = "#Collection(microsoft.graph.bookingWorkTimeSlot)"
			TimeSlots = @(
				@{
					"@odata.type" = "#microsoft.graph.bookingWorkTimeSlot"
					End = "17:00:00.0000000"
					Start = "08:00:00.0000000"
				}
			)
		}
		@{
			"@odata.type" = "#microsoft.graph.bookingWorkHours"
			"Day@odata.type" = "#microsoft.graph.dayOfWeek"
			Day = "wednesday"
			"TimeSlots@odata.type" = "#Collection(microsoft.graph.bookingWorkTimeSlot)"
			TimeSlots = @(
				@{
					"@odata.type" = "#microsoft.graph.bookingWorkTimeSlot"
					End = "17:00:00.0000000"
					Start = "08:00:00.0000000"
				}
			)
		}
		@{
			"@odata.type" = "#microsoft.graph.bookingWorkHours"
			"Day@odata.type" = "#microsoft.graph.dayOfWeek"
			Day = "thursday"
			"TimeSlots@odata.type" = "#Collection(microsoft.graph.bookingWorkTimeSlot)"
			TimeSlots = @(
				@{
					"@odata.type" = "#microsoft.graph.bookingWorkTimeSlot"
					End = "17:00:00.0000000"
					Start = "08:00:00.0000000"
				}
			)
		}
		@{
			"@odata.type" = "#microsoft.graph.bookingWorkHours"
			"Day@odata.type" = "#microsoft.graph.dayOfWeek"
			Day = "friday"
			"TimeSlots@odata.type" = "#Collection(microsoft.graph.bookingWorkTimeSlot)"
			TimeSlots = @(
				@{
					"@odata.type" = "#microsoft.graph.bookingWorkTimeSlot"
					End = "17:00:00.0000000"
					Start = "08:00:00.0000000"
				}
			)
		}
	)
}

New-MgBookingBusinessStaffMember -BookingBusinessId $bookingBusinessId -BodyParameter $params

```