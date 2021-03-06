# Schedule<a name="sam-property-statemachine-schedule"></a>

This object describes an event source with type Schedule

SAM generates [AWS::Events::Rule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-rule.html) resource when this event type is set

## Syntax<a name="sam-property-statemachine-schedule-syntax"></a>

To declare this entity in your AWS SAM template, use the following syntax:

### YAML<a name="sam-property-statemachine-schedule-syntax.yaml"></a>

```
  [Description](#sam-statemachine-schedule-description): String
  [Enabled](#sam-statemachine-schedule-enabled): Boolean
  [Input](#sam-statemachine-schedule-input): String
  [Name](#sam-statemachine-schedule-name): String
  [Schedule](#sam-statemachine-schedule-schedule): String
```

## Properties<a name="sam-property-statemachine-schedule-properties"></a>

 `Description`   <a name="sam-statemachine-schedule-description"></a>
The description of the rule\.  
*Type*: String  
*Required*: No  
*AWS CloudFormation Compatibility*: This property is passed directly to the `[Description](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-rule.html#cfn-events-rule-description)` property of an `AWS::Events::Rule`\.

 `Enabled`   <a name="sam-statemachine-schedule-enabled"></a>
Indicates whether the rule is enabled\.  
If the property is set to False, the rule is disabled  
*Type*: Boolean  
*Required*: No  
*AWS CloudFormation Compatibility*: This property is passed directly to the `[State](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-rule.html#cfn-events-rule-state)` property of an `AWS::Events::Rule`\.

 `Input`   <a name="sam-statemachine-schedule-input"></a>
Valid JSON text passed to the target\. If you use this property, nothing from the event text itself is passed to the target\.  
*Type*: String  
*Required*: No  
*AWS CloudFormation Compatibility*: This property is passed directly to the `[Target](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-target.html#cfn-events-rule-target-input)` property of an `AWS::Events::Rule Target`\.

 `Name`   <a name="sam-statemachine-schedule-name"></a>
The name of the rule\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the rule name\.  
*Type*: String  
*Required*: No  
*AWS CloudFormation Compatibility*: This property is passed directly to the `[Name](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-rule.html#cfn-events-rule-name)` property of an `AWS::Events::Rule`\.

 `Schedule`   <a name="sam-statemachine-schedule-schedule"></a>
The scheduling expression that determines when and how often the rule runs\. For more information, see [Schedule Expressions for Rules](https://docs.aws.amazon.com/eventbridge/latest/userguide/scheduled-events.html)\.  
*Type*: String  
*Required*: Yes  
*AWS CloudFormation Compatibility*: This property is passed directly to the `[ScheduleExpression](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-rule.html#cfn-events-rule-scheduleexpression)` property of an `AWS::Events::Rule`\.

## Examples<a name="sam-property-statemachine-schedule--examples"></a>

### CloudWatch Schedule Event<a name="sam-property-statemachine-schedule--examples--cloudwatch-schedule-event"></a>

CloudWatch Schedule Event Example

#### YAML<a name="sam-property-statemachine-schedule--examples--cloudwatch-schedule-event--yaml"></a>

```
CWSchedule:
  Type: Schedule
  Properties:
    Schedule: 'rate(1 minute)'
    Name: TestSchedule
    Description: test schedule
    Enabled: False
```